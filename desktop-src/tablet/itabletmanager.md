---
description: 提供所有連接至電腦之平板電腦的存取權。
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: ITabletManager 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027502"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="6d53d-103">ITabletManager 介面</span><span class="sxs-lookup"><span data-stu-id="6d53d-103">ITabletManager interface</span></span>

<span data-ttu-id="6d53d-104">提供所有連接至電腦之平板電腦的存取權。</span><span class="sxs-lookup"><span data-stu-id="6d53d-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="6d53d-105">成員</span><span class="sxs-lookup"><span data-stu-id="6d53d-105">Members</span></span>

<span data-ttu-id="6d53d-106">**ITabletManager** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6d53d-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6d53d-107">**ITabletManager** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6d53d-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="6d53d-108">方法</span><span class="sxs-lookup"><span data-stu-id="6d53d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6d53d-109">方法</span><span class="sxs-lookup"><span data-stu-id="6d53d-109">Methods</span></span>

<span data-ttu-id="6d53d-110">**ITabletManager** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6d53d-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="6d53d-111">方法</span><span class="sxs-lookup"><span data-stu-id="6d53d-111">Method</span></span>                                                  | <span data-ttu-id="6d53d-112">描述</span><span class="sxs-lookup"><span data-stu-id="6d53d-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="6d53d-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d53d-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="6d53d-114">抓取指定的 tablet 物件。</span><span class="sxs-lookup"><span data-stu-id="6d53d-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="6d53d-115">**GetTabletCount**</span><span class="sxs-lookup"><span data-stu-id="6d53d-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="6d53d-116">抓取連接至系統的平板電腦數目。</span><span class="sxs-lookup"><span data-stu-id="6d53d-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d53d-117">備註</span><span class="sxs-lookup"><span data-stu-id="6d53d-117">Remarks</span></span>

<span data-ttu-id="6d53d-118">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="6d53d-118">Developers should not use this interface.</span></span>

<span data-ttu-id="6d53d-119">下列程式碼顯示如何實 **ITabletManager** 介面。</span><span class="sxs-lookup"><span data-stu-id="6d53d-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="6d53d-120">呼叫 [](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)具有 CLSID TABLETMANAGERS 類別識別碼的 CoCreateInstance \_ ，然後呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))以取得 **ITabletManager 介面** 的指標。</span><span class="sxs-lookup"><span data-stu-id="6d53d-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="6d53d-121">CLSID \_ TABLETMANAGERS GUID 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="6d53d-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="6d53d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d53d-122">Requirements</span></span>



| <span data-ttu-id="6d53d-123">需求</span><span class="sxs-lookup"><span data-stu-id="6d53d-123">Requirement</span></span> | <span data-ttu-id="6d53d-124">值</span><span class="sxs-lookup"><span data-stu-id="6d53d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d53d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d53d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d53d-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d53d-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6d53d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d53d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d53d-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="6d53d-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6d53d-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d53d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d53d-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d53d-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

