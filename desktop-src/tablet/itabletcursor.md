---
description: 表示手寫筆物件。
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: ITabletCursor 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852567"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="c314f-103">ITabletCursor 介面</span><span class="sxs-lookup"><span data-stu-id="c314f-103">ITabletCursor interface</span></span>

<span data-ttu-id="c314f-104">表示手寫筆物件。</span><span class="sxs-lookup"><span data-stu-id="c314f-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="c314f-105">成員</span><span class="sxs-lookup"><span data-stu-id="c314f-105">Members</span></span>

<span data-ttu-id="c314f-106">**ITabletCursor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c314f-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c314f-107">**ITabletCursor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c314f-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="c314f-108">方法</span><span class="sxs-lookup"><span data-stu-id="c314f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c314f-109">方法</span><span class="sxs-lookup"><span data-stu-id="c314f-109">Methods</span></span>

<span data-ttu-id="c314f-110">**ITabletCursor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c314f-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="c314f-111">方法</span><span class="sxs-lookup"><span data-stu-id="c314f-111">Method</span></span>                                                 | <span data-ttu-id="c314f-112">描述</span><span class="sxs-lookup"><span data-stu-id="c314f-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="c314f-113">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="c314f-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="c314f-114">從 tablet 手寫筆取出指定的按鈕物件。</span><span class="sxs-lookup"><span data-stu-id="c314f-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="c314f-115">**GetButtonCount**</span><span class="sxs-lookup"><span data-stu-id="c314f-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="c314f-116">抓取 tablet 手寫筆上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="c314f-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="c314f-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="c314f-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="c314f-118">抓取手寫筆識別碼。</span><span class="sxs-lookup"><span data-stu-id="c314f-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="c314f-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="c314f-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="c314f-120">捕獲 tablet 手寫筆的名稱。</span><span class="sxs-lookup"><span data-stu-id="c314f-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="c314f-121">**IsInverted**</span><span class="sxs-lookup"><span data-stu-id="c314f-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="c314f-122">指出手寫筆是否已反轉。</span><span class="sxs-lookup"><span data-stu-id="c314f-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c314f-123">備註</span><span class="sxs-lookup"><span data-stu-id="c314f-123">Remarks</span></span>

<span data-ttu-id="c314f-124">請勿使用這個介面。</span><span class="sxs-lookup"><span data-stu-id="c314f-124">Do not use this interface.</span></span>

<span data-ttu-id="c314f-125">下列程式碼說明如何定義 **ITabletCursor** 介面。</span><span class="sxs-lookup"><span data-stu-id="c314f-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="c314f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c314f-126">Requirements</span></span>



| <span data-ttu-id="c314f-127">需求</span><span class="sxs-lookup"><span data-stu-id="c314f-127">Requirement</span></span> | <span data-ttu-id="c314f-128">值</span><span class="sxs-lookup"><span data-stu-id="c314f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c314f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c314f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c314f-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c314f-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c314f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c314f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c314f-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="c314f-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c314f-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c314f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c314f-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c314f-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

