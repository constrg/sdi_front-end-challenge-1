<script setup>
import news from '../data/news.json'
import NewsPages from './NewsPages.vue';

const current_news = news.slice(0, 1)

</script>

<template>
    <div class="news">
        <div class="container">
            <div class="news_content">
                <div class="news_list">
                    <ul v-for="news_item in current_news" :key="news_item.id">
                        <div class="news_info">
                        <img :src="news_item.image_url" class="news_info_image" alt="">
                                <div class="date_container">
                                    <div class="date">
                                        <span class="day">13</span>
                                    <span class="month">JAN</span>
                                    </div>
                                </div>
                            <div class="share_container">
                                <a href="#" class="share_link"><img src="../assets/share.png" class="share_icon" alt="">SHARE</a>
                            </div>
                            <span class="news_info_author">{{news_item.name}}</span>
                            <h1 class="news_info_title">{{ news_item.title }}</h1>
                            <p class="news_info_body">{{ news_item.body }}</p>
                            <a href="#" class="read_article_link">Read Article</a>
                        </div>     
                    </ul>
                </div>
            <NewsPages />
            </div>
        </div>
    </div>
</template>

<style scoped>


.news 
{
    height: 100%;
    padding-block: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.news .news_content 
{    
    padding: 20px;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}
.news .news_content .news_title 
{
    font-size: 40px;
    color: var(--red);
}
.news .news_content .news_list 
{
    margin-bottom: 20px
}

.news .news_content .news_list .news_info
{
    background-color: var(--light);
    height: 100%;
}

.news .news_content .news_list .news_info .news_info_image 
{
    width: 100%;
    object-fit: cover;
    height: 300px;
}

.news .news_content .news_list .news_info .date_container
{
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    
}

.news .news_content .news_list .news_info .date_container .date
{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 10px 25px;
    background-color: var(--red);
    clip-path: polygon(15% 0, 100% 0%, 85% 100%, 0% 100%);
    color: var(--light);
    position: relative;
    text-align: center;
    margin-top: -45px;
    margin-bottom: 10px;
    margin-left: 20px
}

.news .news_content .news_list .news_info .date_container .date::after{
    content: "";
    background-color: var(--light);
    clip-path: polygon(100% 80%, 80% 100%, 100% 100%);
    width: 40px;
    height: 40px;
    display: block;
    position: absolute;
    bottom: 5px;
    right: 13px;
}
.news .news_content .news_list .news_info .date_container .date .day 
{
    font-size: 20px;
    font-weight: 700;
}

.news .news_content .news_list .news_info .date_container .date .month 
{
    font-size: 10px;
    margin-top: -3px;
}

.news .news_content .news_list .news_info .share_container {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    position: relative;
    align-items: flex-end;
}

.news .news_content .news_list .news_info .share_container::after
{
    content: "";
    background-color: var(--gray);
    width: 100%;
    height: 1px;
    display: block;
    opacity: 10%;
    margin-top: 10px;
}


.news .news_content .news_list .news_info .share_container .share_link
{
    color: var(--dark);
    font-size: 12px;
    font-weight: 500;
    display: flex;
    justify-content: center;
    align-items: center;
    column-gap: 3px;
}

.news .news_content .news_list .news_info .share_container .share_link .share_icon
{
    width: 14px;
}

.news .news_content .news_list .news_info .news_info_author 
{
    color: var(--red);
    font-weight: 700;
    font-size: 14px;
}
.news .news_content .news_list .news_info .news_info_title
{
    font-size: 25px;
    font-weight: 700;
    margin-bottom: 20px;
}

.news .news_content .news_list .news_info .news_info_body
{
    font-size: 13px;
    margin-bottom: 20px;
    color: var(--gray);
}

.news .news_content .news_list .news_info .read_article_link
{
    font-weight: 700;
    text-decoration: underline;
    color: var(--dark);
    font-size: 14px;
}

</style>