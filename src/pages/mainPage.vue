<template>
  <f7-page name="main">
    <f7-navbar>
      <f7-nav-center sliding>Framework7</f7-nav-center>
      <f7-nav-right>
        <f7-link icon="icon-bars" open-panel="right"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>Welcome to Framework7</f7-block-title>
    <f7-block>
      <f7-button href="/about/">About Framework7</f7-button>
    </f7-block>
    <f7-block-title>FRAMEWORK7 KITCHEN SINK</f7-block-title>
    <f7-list v-for="list in lists" :key="list.id">
      <f7-list-item v-for="(item, index) in list.items"
        link-ignore-cache
        media="<i class='icon icon-f7'></i>"
        :link="item.link"
        :title="item.title"
        :class="item.class"
        :badge="item.badge"
        :badge-color="item.badgeColor"
        :key="index"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      lists: [
        {
          id: 'items1',
          items: [
            {
              title: '可折叠的',
              link: '/accordion/',
              badge: '',
              badgeColor: ''
            }, {
              title: '自动补全',
              link: '/autocomplete/',
              badge: '',
              badgeColor: ''
            }, {
              title: '日历选择',
              link: '/calendarDatepicker/',
              badge: '',
              badgeColor: ''
            }, {
              title: '展示卡',
              link: '/cards/',
              badge: '',
              badgeColor: ''
            }, {
              title: '芯片/标签',
              link: '/chipsTags/',
              badge: '',
              badgeColor: ''
            }, {
              title: '联系人列表',
              link: '/contacts/',
              badge: '',
              badgeColor: ''
            }, {
              title: '浮动操作按钮',
              link: '/floatingAction/',
              badge: '',
              badgeColor: ''
            }, {
              title: '表格',
              link: '/forms/',
              badge: '',
              badgeColor: ''
            }, {
              title: '栅格',
              link: '/grid/',
              badge: '',
              badgeColor: ''
            }, {
              title: '图标',
              link: '/icons/',
              badge: '258',
              badgeColor: 'green'
            }, {
              title: '无限滚动条',
              link: '/infiniteScroll/',
              badge: '',
              badgeColor: ''
            }, {
              title: '懒加载图片',
              link: '/lazyLoadImages/',
              badge: '',
              badgeColor: ''
            }, {
              title: '列表视图',
              link: '/listView/',
              badge: '',
              badgeColor: ''
            }, {
              title: '登陆界面',
              link: '/loginScreen/',
              badge: '',
              badgeColor: ''
            }, {
              title: '多媒体列表',
              link: '/mediaLists/',
              badge: '',
              badgeColor: ''
            }, {
              title: '消息',
              link: '/messages/',
              badge: '',
              badgeColor: ''
            }, {
              title: '动态弹框',
              link: '/modals/',
              badge: '',
              badgeColor: ''
            }, {
              title: '导航和工具条',
              link: '/navbarsAndToolbars/',
              badge: '',
              badgeColor: ''
            }, {
              title: '通知',
              link: '/notifications/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Photo Browser',
              link: '/photoBrowser/',
              badge: '',
              badgeColor: ''
            }, {
              title: '选择器',
              link: '/picker/',
              badge: '',
              badgeColor: ''
            }, {
              title: '弹出选择框',
              link: '/popover/',
              badge: '',
              badgeColor: ''
            }, {
              title: '正在加载',
              link: '/preloader/',
              badge: '',
              badgeColor: ''
            }, {
              title: '进度条',
              link: '/progressBar/',
              badge: '',
              badgeColor: ''
            }, {
              title: '下拉刷新',
              link: '/pullToRefresh/',
              badge: '',
              badgeColor: ''
            }, {
              title: '搜索条',
              link: '/searchBar/',
              badge: '',
              badgeColor: ''
            }, {
              title: '侧面板',
              link: '/sidePanels/',
              badge: '',
              badgeColor: ''
            }, {
              title: '分类列表',
              link: '/sortableList/',
              badge: '',
              badgeColor: ''
            }, {
              title: '滑动删除',
              link: '/swipeToDelete/',
              badge: '',
              badgeColor: ''
            }, {
              title: '滑动效果',
              link: '/swiperSlider/',
              badge: '',
              badgeColor: ''
            }, {
              title: '选项卡',
              link: '/tabs/',
              badge: '',
              badgeColor: ''
            }, {
              title: '时间轴',
              link: '/timeline/',
              badge: '',
              badgeColor: ''
            }, {
              title: '虚拟列表',
              link: '/virtualList/',
              badge: '',
              badgeColor: ''
            }
          ]
        }, {
          id: 'items2',
          items: [
            {
              title: '动画效果',
              link: '/animation/',
              badge: '',
              badgeColor: ''
            }, {
              title: '颜色主题',
              link: '/colorThemes/',
              badge: '',
              badgeColor: ''
            }, {
              title: '动态创建页面',
              link: '#',
              class: 'ks-generate-page',
              badge: '',
              badgeColor: ''
            }
          ]
        }, {
          id: 'items3',
          items: [
            {
              title: '视图转换 And 效果',
              link: '/transitions/',
              badge: '',
              badgeColor: ''
            }, {
              title: '产品核心特点',
              link: '/coreFeatures/',
              badge: '',
              badgeColor: ''
            }
          ]
        }
      ]
    }
  },
  mounted () {
    var dynamicPageIndex = 0
    var self = this

    function createContentPage() {
      self.$router.loadContent(
        '<!-- Top Navbar-->' +
        '<div class="navbar">' +
        '  <div class="navbar-inner">' +
        '    <div class="left sliding"><a href="#" class="back link"><i class="icon icon-back"></i><span>Back</span></a></div>' +
        '    <div class="center sliding">Dynamic Page ' + (++dynamicPageIndex) + '</div>' +
        '  </div>' +
        '</div>' +
        '<div class="pages">' +
        '  <!-- Page, data-page contains page name-->' +
        '  <div data-page="dynamic-content" class="page">' +
        '    <!-- Scrollable page content-->' +
        '    <div class="page-content">' +
        '      <div class="content-block">' +
        '        <div class="content-block-inner">' +
        '          <p>Here is a dynamic page created on ' + new Date() + ' !</p>' +
        '          <p>Go <a href="#" class="back">back</a> or generate <a href="#" class="ks-generate-page">one more page</a>.</p>' +
        '        </div>' +
        '      </div>' +
        '    </div>' +
        '  </div>' +
        '</div>'
      )
      return
    }

    this.$$(document).on('click', '.ks-generate-page', createContentPage)
  }
}
</script>