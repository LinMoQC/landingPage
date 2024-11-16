<script setup lang="ts">
import dark_chart_writing from '@images/front-pages/landing-page/dark-chart-writing.png'
import dark_content_writing from '@images/front-pages/landing-page/dark-content-writing.png'
import dark_online_writing from '@images/front-pages/landing-page/dark-online-writing.png'
import dark_paragraph_polishing from '@images/front-pages/landing-page/dark-paragraph-polishing.png'
import white_chart_writing from '@images/front-pages/landing-page/white-chart-writing.png'
import white_content_writing from '@images/front-pages/landing-page/white-content-writing.png'
import white_online_writing from '@images/front-pages/landing-page/white-online-writing.png'
import white_paragraph_polishing from '@images/front-pages/landing-page/white-paragraph-polishing.png'
import { VBtn } from 'vuetify/components'

const dark = [
    {
        img: dark_content_writing,
        title: '文段润色',
        content: '独创学术表达数据库，智能润色，一键学术风格专家级表达。'
    },
    {
        img: dark_online_writing,
        title: '内容写作',
        content: '文献阅读过于麻烦？导入文献，粘贴提纲，论文综述一气呵成。'
    },
    {
        img: dark_paragraph_polishing,
        title: '图表写作',
        content: '图表阅读晕头转向？专有图表解读大模型，数据规律一键解读，组会汇报效率upup！'
    },
    {
        img: dark_chart_writing,
        title: '在线写作',
        content: '在线智能写作，参考文献一键匹配，内容随心写。'
    },
]

const white = [
    {
        img: white_content_writing,
        title: '文段润色',
        content: '独创学术表达数据库，智能润色，一键学术风格专家级表达。'
    },
    {
        img: white_online_writing,
        title: '内容写作',
        content: '文献阅读过于麻烦？导入文献，粘贴提纲，论文综述一气呵成。'
    },
    {
        img: white_paragraph_polishing,
        title: '图表写作',
        content: '图表阅读晕头转向？专有图表解读大模型，数据规律一键解读，组会汇报效率upup！'
    },
    {
        img: white_chart_writing,
        title: '在线写作',
        content: '在线智能写作，参考文献一键匹配，内容随心写。'
    },
]

</script>

<template>
    <VContainer id="functions">
        <div class="functions-cards">
            <div class="headers d-flex justify-center flex-column align-center mb-12">
                <VChip label color="primary" class="mb-4" size="small">
                    Functions
                </VChip>
                <div class="d-flex text-h4 mb-1 align-center flex-wrap justify-center">
                    <div class="position-relative me-2">
                        <div class="section-title">
                            两大功能 文献阅读写作一气呵成
                        </div>
                    </div>
                </div>
                <p class="text-body-1 mb-0">
                    高频使用功能单列 使用便捷
                </p>

                <VRow>
                    <VCol v-for="(item, index) in dark" :key="index" cols="12" class="d-flex padding-contain">
                        <template v-if="index % 2 === 0">
                            <div class="left-content">
                                <div class="icon mb-4">
                                    <VIcon color="primary" size="48">mdi-file-document-outline</VIcon>
                                </div>
                                <h2 class="title">
                                    {{ item.title }}
                                </h2>
                                <p class="description" style="width: 15rem;">
                                    {{ item.content }}
                                </p>
                                <VBtn color="primary" class="mt-4" outlined>
                                    点击使用 →
                                </VBtn>
                            </div>
                            <img :src="item.img" alt="Functions Image" class="mx-auto mb-4"
                                style="max-width: 600px; height: 400px; object-fit: cover; width: 100%;" />
                        </template>

                        <template v-else>
                            <img :src="item.img" alt="Functions Image" class="mx-auto mb-4"
                                style="max-width: 600px; height: 400px; object-fit: cover; width: 100%;" />
                            <div class="right-content ms-4">
                                <div class="icon mb-4">
                                    <VIcon color="primary" size="48">mdi-file-document-outline</VIcon>
                                </div>
                                <h2 class="title">
                                    {{ item.title }}
                                </h2>
                                <p class="description" style="width: 15rem;">
                                    {{ item.content }}
                                </p>
                                <VBtn color="primary" class="mt-4" outlined>
                                    ← 点击使用
                                </VBtn>
                            </div>
                        </template>
                    </VCol>
                </VRow>


            </div>
        </div>
    </VContainer>

</template>

<style lang="scss" scoped>
.padding-contain {
    padding: 5rem;
}

.left-content {
    width: 50%;

    .title {
        font-size: 32px;
        font-weight: 600;
        margin-bottom: 16px;
    }

    .description {
        font-size: 16px;
        line-height: 1.5;
    }
}

@media (max-width: 600px) {
    .left-content {
        display: none;
    }

    .right-content {
        display: none;
    }
}

.right-content {
    width: 50%;
    float: right;
    display: flex;
    flex-direction: column;
    align-items: flex-end;

    .title {
        font-size: 32px;
        font-weight: 600;
        margin-bottom: 16px;
    }

    .description {
        font-size: 16px;
        line-height: 1.5;
    }

    .v-btn {
        margin-top: 16px;
    }
}


.functions-cards {
    margin-block: 6.625rem 3.75rem;
    overflow-x: hidden;
}

.section-title::after {
    position: absolute;
    background: url("../../../assets/images/front-pages/icons/section-title-icon.png") no-repeat left bottom;
    background-size: contain;
    block-size: 100%;
    content: "";
    inline-size: 120%;
    inset-block-end: 0;
    inset-inline-start: -12%;
}

.section-title {
    font-size: 24px;
    font-weight: 800;
    line-height: 36px;
}
</style>
