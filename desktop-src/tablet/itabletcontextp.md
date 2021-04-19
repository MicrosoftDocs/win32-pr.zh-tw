---
description: 表示 tablet 內容。
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: ITabletCoNtextP 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975524"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="b205c-103">ITabletCoNtextP 介面</span><span class="sxs-lookup"><span data-stu-id="b205c-103">ITabletContextP interface</span></span>

<span data-ttu-id="b205c-104">表示 tablet 內容。</span><span class="sxs-lookup"><span data-stu-id="b205c-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="b205c-105">成員</span><span class="sxs-lookup"><span data-stu-id="b205c-105">Members</span></span>

<span data-ttu-id="b205c-106">**ITabletCoNtextP** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b205c-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b205c-107">**ITabletCoNtextP** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b205c-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="b205c-108">方法</span><span class="sxs-lookup"><span data-stu-id="b205c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b205c-109">方法</span><span class="sxs-lookup"><span data-stu-id="b205c-109">Methods</span></span>

<span data-ttu-id="b205c-110">**ITabletCoNtextP** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b205c-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="b205c-111">方法</span><span class="sxs-lookup"><span data-stu-id="b205c-111">Method</span></span>                                                                                           | <span data-ttu-id="b205c-112">描述</span><span class="sxs-lookup"><span data-stu-id="b205c-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="b205c-113">**IsTopMostHook**</span><span class="sxs-lookup"><span data-stu-id="b205c-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="b205c-114">指出 tablet 內容是否在最上層的掛勾中。</span><span class="sxs-lookup"><span data-stu-id="b205c-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="b205c-115">**重疊**</span><span class="sxs-lookup"><span data-stu-id="b205c-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="b205c-116">將 tablet 內容移至輸入佇列的前端或背面。</span><span class="sxs-lookup"><span data-stu-id="b205c-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="b205c-117">**TrackInputRect**</span><span class="sxs-lookup"><span data-stu-id="b205c-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="b205c-118">將 tablet 數位板更新為視窗位置對應座標。</span><span class="sxs-lookup"><span data-stu-id="b205c-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="b205c-119">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="b205c-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="b205c-120">提供 tablet 執行緒之間共用記憶體的存取。</span><span class="sxs-lookup"><span data-stu-id="b205c-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="b205c-121">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="b205c-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="b205c-122">提供 tablet 執行緒之間共用記憶體的存取。</span><span class="sxs-lookup"><span data-stu-id="b205c-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="b205c-123">備註</span><span class="sxs-lookup"><span data-stu-id="b205c-123">Remarks</span></span>

<span data-ttu-id="b205c-124">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="b205c-124">Developers should not use this interface.</span></span>

<span data-ttu-id="b205c-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) 僅適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b205c-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="b205c-126">下列程式碼說明如何定義 **ITabletCoNtextP** 介面。</span><span class="sxs-lookup"><span data-stu-id="b205c-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="b205c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b205c-127">Requirements</span></span>



| <span data-ttu-id="b205c-128">需求</span><span class="sxs-lookup"><span data-stu-id="b205c-128">Requirement</span></span> | <span data-ttu-id="b205c-129">值</span><span class="sxs-lookup"><span data-stu-id="b205c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b205c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b205c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b205c-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b205c-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b205c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b205c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b205c-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="b205c-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b205c-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="b205c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b205c-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b205c-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

