---
description: 代表連接到電腦的平板電腦。
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: ITablet 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971495"
---
# <a name="itablet-interface"></a><span data-ttu-id="87e51-103">ITablet 介面</span><span class="sxs-lookup"><span data-stu-id="87e51-103">ITablet interface</span></span>

<span data-ttu-id="87e51-104">代表連接到電腦的平板電腦。</span><span class="sxs-lookup"><span data-stu-id="87e51-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="87e51-105">成員</span><span class="sxs-lookup"><span data-stu-id="87e51-105">Members</span></span>

<span data-ttu-id="87e51-106">**ITablet** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="87e51-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87e51-107">**ITablet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87e51-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="87e51-108">方法</span><span class="sxs-lookup"><span data-stu-id="87e51-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="87e51-109">方法</span><span class="sxs-lookup"><span data-stu-id="87e51-109">Methods</span></span>

<span data-ttu-id="87e51-110">**ITablet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="87e51-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="87e51-111">方法</span><span class="sxs-lookup"><span data-stu-id="87e51-111">Method</span></span>                                                                 | <span data-ttu-id="87e51-112">描述</span><span class="sxs-lookup"><span data-stu-id="87e51-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="87e51-113">**CreateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="87e51-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="87e51-114">建立描述指定之平板電腦裝置的內容物件。</span><span class="sxs-lookup"><span data-stu-id="87e51-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="87e51-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87e51-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="87e51-116">抓取指定的 [**ITabletCursor**](itabletcursor.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="87e51-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="87e51-117">**GetCursorCount**</span><span class="sxs-lookup"><span data-stu-id="87e51-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="87e51-118">捕獲與平板電腦相關聯的資料指標物件數目。</span><span class="sxs-lookup"><span data-stu-id="87e51-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="87e51-119">**GetDefaultCoNtextSettings**</span><span class="sxs-lookup"><span data-stu-id="87e51-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="87e51-120">捕獲平板電腦的預設內容設定。</span><span class="sxs-lookup"><span data-stu-id="87e51-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="87e51-121">**GetHardwareCaps**</span><span class="sxs-lookup"><span data-stu-id="87e51-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="87e51-122">抓取代表平板電腦硬體功能的值。</span><span class="sxs-lookup"><span data-stu-id="87e51-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="87e51-123">**GetMaxInputRect**</span><span class="sxs-lookup"><span data-stu-id="87e51-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="87e51-124">抓取代表平板電腦最大輸入區域的矩形。</span><span class="sxs-lookup"><span data-stu-id="87e51-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="87e51-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="87e51-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="87e51-126">抓取包含 tablet 裝置名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="87e51-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="87e51-127">**GetPlugAndPlayId**</span><span class="sxs-lookup"><span data-stu-id="87e51-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="87e51-128">抓取包含平板電腦裝置之隨插即用識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="87e51-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="87e51-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87e51-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="87e51-130">取得指定之屬性的度量資料。</span><span class="sxs-lookup"><span data-stu-id="87e51-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="87e51-131">備註</span><span class="sxs-lookup"><span data-stu-id="87e51-131">Remarks</span></span>

<span data-ttu-id="87e51-132">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="87e51-132">Developers should not use this interface.</span></span>

<span data-ttu-id="87e51-133">下列程式碼說明如何定義 **ITablet** 介面。</span><span class="sxs-lookup"><span data-stu-id="87e51-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="87e51-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="87e51-134">Requirements</span></span>



| <span data-ttu-id="87e51-135">需求</span><span class="sxs-lookup"><span data-stu-id="87e51-135">Requirement</span></span> | <span data-ttu-id="87e51-136">值</span><span class="sxs-lookup"><span data-stu-id="87e51-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e51-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87e51-137">Minimum supported client</span></span><br/> | <span data-ttu-id="87e51-138">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87e51-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="87e51-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87e51-139">Minimum supported server</span></span><br/> | <span data-ttu-id="87e51-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="87e51-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="87e51-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="87e51-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="87e51-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87e51-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

