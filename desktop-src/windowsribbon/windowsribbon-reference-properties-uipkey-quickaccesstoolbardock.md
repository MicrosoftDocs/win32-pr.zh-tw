---
title: UI_PKEY_QuickAccessToolbarDock
description: 識別 UI \_ PKEY \_ QuickAccessToolbarDock 屬性。
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375480"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="8ad60-103">UI \_ PKEY \_ QuickAccessToolbarDock</span><span class="sxs-lookup"><span data-stu-id="8ad60-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="8ad60-104">識別 UI \_ PKEY \_ QuickAccessToolbarDock 屬性。</span><span class="sxs-lookup"><span data-stu-id="8ad60-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="8ad60-105">備註</span><span class="sxs-lookup"><span data-stu-id="8ad60-105">Remarks</span></span>

<span data-ttu-id="8ad60-106">\_ \_ 應用程式會使用 UI PKEY QuickAccessToolbarDock 來查詢快速存取工具列 (QAT) 的停駐狀態。</span><span class="sxs-lookup"><span data-stu-id="8ad60-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="8ad60-107">屬性值來自 [**UI \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) 列舉。</span><span class="sxs-lookup"><span data-stu-id="8ad60-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad60-108">UI \_ CONTROLDOCK \_ TOP</span><span class="sxs-lookup"><span data-stu-id="8ad60-108">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="8ad60-109">QAT 會停駐在功能區主機應用程式的非工作區中，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="8ad60-109">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![[快速存取] 工具列的螢幕擷取畫面，停駐在非工作區的功能區上方。](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="8ad60-111">UI \_ CONTROLDOCK \_ 底部</span><span class="sxs-lookup"><span data-stu-id="8ad60-111">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="8ad60-112">QAT 會停駐為功能區下方的視覺化整數寬線，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="8ad60-112">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![快速存取工具列上停駐于功能區下方的螢幕擷取畫面。](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="8ad60-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ad60-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad60-115">功能區屬性</span><span class="sxs-lookup"><span data-stu-id="8ad60-115">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

