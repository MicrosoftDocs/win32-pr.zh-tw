---
description: 表示手寫筆裝置上按鈕的一般資訊。
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: ITabletCursorButton 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319723"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="47940-103">ITabletCursorButton 介面</span><span class="sxs-lookup"><span data-stu-id="47940-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="47940-104">表示手寫筆裝置上按鈕的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="47940-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="47940-105">成員</span><span class="sxs-lookup"><span data-stu-id="47940-105">Members</span></span>

<span data-ttu-id="47940-106">**ITabletCursorButton** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="47940-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47940-107">**ITabletCursorButton** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="47940-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="47940-108">方法</span><span class="sxs-lookup"><span data-stu-id="47940-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47940-109">方法</span><span class="sxs-lookup"><span data-stu-id="47940-109">Methods</span></span>

<span data-ttu-id="47940-110">**ITabletCursorButton** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="47940-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="47940-111">方法</span><span class="sxs-lookup"><span data-stu-id="47940-111">Method</span></span>                                         | <span data-ttu-id="47940-112">描述</span><span class="sxs-lookup"><span data-stu-id="47940-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="47940-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="47940-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="47940-114">抓取手寫筆按鈕的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="47940-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="47940-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="47940-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="47940-116">抓取手寫筆按鈕的名稱。</span><span class="sxs-lookup"><span data-stu-id="47940-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="47940-117">備註</span><span class="sxs-lookup"><span data-stu-id="47940-117">Remarks</span></span>

<span data-ttu-id="47940-118">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="47940-118">Developers should not use this interface.</span></span>

<span data-ttu-id="47940-119">下列程式碼說明如何定義 **ITabletCursorButton** 介面。</span><span class="sxs-lookup"><span data-stu-id="47940-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="47940-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="47940-120">Requirements</span></span>



| <span data-ttu-id="47940-121">需求</span><span class="sxs-lookup"><span data-stu-id="47940-121">Requirement</span></span> | <span data-ttu-id="47940-122">值</span><span class="sxs-lookup"><span data-stu-id="47940-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47940-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47940-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47940-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47940-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="47940-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47940-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47940-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="47940-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47940-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="47940-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="47940-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47940-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47940-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47940-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47940-130">**ITabletCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="47940-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

