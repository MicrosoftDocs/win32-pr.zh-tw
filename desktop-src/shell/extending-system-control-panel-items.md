---
description: 在主控台中找到的某些系統專案是可擴充的。 若要安裝主控台擴充功能，請依照下列方式註冊您的 Shell 擴充功能，其中 name 是系統專案的預先定義名稱 (請參閱下表) 。
title: 擴充系統主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469745"
---
# <a name="extending-system-control-panel-items"></a>擴充系統主控台專案

在主控台中找到的某些系統專案是可擴充的。 若要安裝主控台擴充功能，請依照下列方式註冊您的 Shell 擴充功能，其中 *name* 是系統專案的預先定義名稱 (請參閱下表) 。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

這與您針對預先定義的 Shell 物件註冊擴充功能的方式類似。 因為主控台專案所支援的唯一 Shell 擴充功能是屬性工作表，所以註冊必須在 **shellex** PropertySheetHandlers 子機碼下 \\  。




| 主控台專案 | <em>name</em> | 備註 | 
|--------------------|---------------|---------|
| 顯示 | 桌子 | 也支援取代 <strong>桌面</strong> 網頁。<blockquote>[!Note]<br />Windows Vista 中已不再支援此功能。</blockquote><br /> | 
| 顯示設定 Advanced | 裝置 | Nonhardware 特定的 advanced 屬性。<blockquote>[!Note]<br />Windows Vista 中已不再支援此功能。</blockquote><br /> | 
| 顯示設定 Advanced | 顯示 | 硬體特定的 advanced 屬性。<blockquote>[!Note]<br />Windows Vista 中已不再支援此功能。</blockquote><br /> | 
| 網際網路選項 | 網際網路 | 延伸模組頁面的最大數目為18。 | 
| 鍵盤 | 鍵盤 | 延伸頁面的最大數目為30。 | 
| 滑鼠 | 滑鼠 | 也支援取代標準頁面。 延伸模組頁面的數目上限為8。 | 
| 電源選項 | 電源 | 頁面數目上限（包括標準頁面）為18。 | 
| 系統 | 系統 | 延伸模組頁面的數目上限為8。<blockquote>[!Note]<br />Windows Vista 中已不再支援此功能。</blockquote><br /> | 




 

Windows XP 主控台中的 [**新增或移除程式**] 專案不是屬性工作表，因此無法透過此處討論的方法來擴充。 相反地，它的內容是從應用程式發行者取得的。 如需有關新增內容至 **新增或移除程式** 的詳細資訊，請參閱 [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher)、 [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)和 [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[在 Windows Vista 下存取保管庫模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




