<template>
<style>
        body {
            font-family: Arial, sans-serif;
        }
        h2 {
            font-size: 16px;
            margin-bottom: 10px;
        }
        ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }
        li {
            display: inline;
            margin-right: 16px;
        }
        a {
            text-decoration: none;
            color: #333;
            font-size: 16px;
        }

        /* 响应式设计 */
        @media only screen and (max-width: 600px) {
            h2 {
                font-size: 16px;
            }
            li {
                display: block;
                margin-bottom: 10px;
            }
        }
    </style>
    <h2>友情链接</h2>
    <ul>
        <li><a href="https://example.com">友情链接 1</a></li>
        <li><a href="https://example.net">友情链接 2</a></li>
        <li><a href="https://example.org">友情链接 3</a></li>
    </ul>
	<footer class="text-left text-[#6c757d] p-6 bg-[rgba(248,249,250,1)] h-[70px]">
	
		<section class="flex justify-center">
			<!-- Left -->
			<div class="text-[14px] h-[30px]">
				<span
					>© 2024 
					
					<a
						href="https://fanghai.site"
						target="_blank"
						class="decoration-transparent text-[#000]"
						>FANGHAI</a
					>
				</span>
				
			</div>
			<!-- Left -->

			<div v-if="footerConfig.right.is_show" class="flex-grow"></div>
			<!-- Right -->
			<div
				v-if="footerConfig.right.is_show && footerConfig.right.list.length > 0"
				class="flex text-[20px] text-black"
			>
				<a v-for="item in footerConfig.right.list" :href="item.url" target="_blank" class="pr-6">
					<IconsFontAwesome
						:size="item.icon_size"
						class="hover:text-[#0d6efd]"
						:icon="item.icon_class"
					/>
				</a>
			</div>
		</section>
		
	</footer>
<script charset="UTF-8" id="LA_COLLECT" src="//sdk.51.la/js-sdk-pro.min.js?id=3I4zYs7ZEPySWup4&ck=3I4zYs7ZEPySWup4"></script>
</template>

<script setup lang="ts">
import { CONFIG_KEY_FOOTER, getConfigItem } from '~/stores/config'

const footerConfig = getConfigItem(CONFIG_KEY_FOOTER)
</script>

<style scoped></style>
