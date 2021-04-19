---
description: ITablet3 介面啟用多點觸控查詢以進行輸入。
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: ITablet3 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997946"
---
# <a name="itablet3-interface"></a><span data-ttu-id="4b29f-103">ITablet3 介面</span><span class="sxs-lookup"><span data-stu-id="4b29f-103">ITablet3 interface</span></span>

<span data-ttu-id="4b29f-104">ITablet3 介面啟用多點觸控查詢以進行輸入。</span><span class="sxs-lookup"><span data-stu-id="4b29f-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="4b29f-105">成員</span><span class="sxs-lookup"><span data-stu-id="4b29f-105">Members</span></span>

<span data-ttu-id="4b29f-106">**ITablet3** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="4b29f-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4b29f-107">**ITablet3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4b29f-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="4b29f-108">方法</span><span class="sxs-lookup"><span data-stu-id="4b29f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b29f-109">方法</span><span class="sxs-lookup"><span data-stu-id="4b29f-109">Methods</span></span>

<span data-ttu-id="4b29f-110">**ITablet3** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4b29f-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="4b29f-111">方法</span><span class="sxs-lookup"><span data-stu-id="4b29f-111">Method</span></span>                                                  | <span data-ttu-id="4b29f-112">描述</span><span class="sxs-lookup"><span data-stu-id="4b29f-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="4b29f-113">**GetMaximumCursors**</span><span class="sxs-lookup"><span data-stu-id="4b29f-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="4b29f-114">抓取支援的輸入數目上限。</span><span class="sxs-lookup"><span data-stu-id="4b29f-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="4b29f-115">**isMultiTouch**</span><span class="sxs-lookup"><span data-stu-id="4b29f-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="4b29f-116">指出是否已啟用此物件的多點觸控功能。</span><span class="sxs-lookup"><span data-stu-id="4b29f-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b29f-117">備註</span><span class="sxs-lookup"><span data-stu-id="4b29f-117">Remarks</span></span>

<span data-ttu-id="4b29f-118">開發人員不應使用此介面</span><span class="sxs-lookup"><span data-stu-id="4b29f-118">Developers should not use this interface</span></span>

<span data-ttu-id="4b29f-119">下列程式碼說明如何定義 **ITablet3** 介面。</span><span class="sxs-lookup"><span data-stu-id="4b29f-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="4b29f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b29f-120">Requirements</span></span>



| <span data-ttu-id="4b29f-121">需求</span><span class="sxs-lookup"><span data-stu-id="4b29f-121">Requirement</span></span> | <span data-ttu-id="4b29f-122">值</span><span class="sxs-lookup"><span data-stu-id="4b29f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b29f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b29f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b29f-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b29f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b29f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b29f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b29f-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b29f-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b29f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b29f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b29f-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b29f-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

