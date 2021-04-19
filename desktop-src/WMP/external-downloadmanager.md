---
title: DownloadManager
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 DownloadManager 屬性會捕獲 DownloadManager 物件。
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- DownloadManager Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992946"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="55dda-106">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="55dda-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="55dda-107">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="55dda-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="55dda-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="55dda-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="55dda-109">**DownloadManager** 屬性會捕獲 **DownloadManager** 物件。</span><span class="sxs-lookup"><span data-stu-id="55dda-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="55dda-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="55dda-110">Possible Values</span></span>

<span data-ttu-id="55dda-111">這個屬性是唯讀的 **DownloadManager** 物件。</span><span class="sxs-lookup"><span data-stu-id="55dda-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55dda-112">備註</span><span class="sxs-lookup"><span data-stu-id="55dda-112">Remarks</span></span>

<span data-ttu-id="55dda-113">在 Windows Media Player 10 或更新版本中， **DownloadManager** 屬性和物件只能從 [線上商店服務] 工作窗格存取。</span><span class="sxs-lookup"><span data-stu-id="55dda-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="55dda-114">您無法使用 **外部** 物件可用之其他功能的 **DownloadManager** ，例如 HTMLView、資訊中心視圖和專輯資訊。</span><span class="sxs-lookup"><span data-stu-id="55dda-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55dda-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="55dda-115">Requirements</span></span>



| <span data-ttu-id="55dda-116">需求</span><span class="sxs-lookup"><span data-stu-id="55dda-116">Requirement</span></span> | <span data-ttu-id="55dda-117">值</span><span class="sxs-lookup"><span data-stu-id="55dda-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55dda-118">版本</span><span class="sxs-lookup"><span data-stu-id="55dda-118">Version</span></span><br/> | <span data-ttu-id="55dda-119">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="55dda-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="55dda-120">DLL</span><span class="sxs-lookup"><span data-stu-id="55dda-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="55dda-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55dda-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55dda-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55dda-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55dda-123">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="55dda-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





