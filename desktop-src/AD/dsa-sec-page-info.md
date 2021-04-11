---
title: DSA_SEC_PAGE_INFO 結構
description: 搭配使用 WM \_ ADSPROP \_ 工作表 \_ 建立和 WM \_ DSA \_ 工作表 \_ 建立 \_ 通知訊息，以在 Active Directory MMC 嵌入式管理單元中定義次要屬性工作表。
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO 結構 Active Directory
- PDSA_SEC_PAGE_INFO 結構指標 Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934640"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="fba4f-105">DSA \_ 秒 \_ 頁面 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="fba4f-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="fba4f-106">[ **DSA \_ SEC] \_ 頁面 \_ 資訊** 結構可搭配 [ [**wm \_ ADSPROP \_ 工作表 \_ 建立**](wm-adsprop-sheet-create.md) ] 和 [ [**WM \_ DSA \_ 工作表] \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md) 訊息，以在 Active Directory MMC 嵌入式管理單元中定義次要屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="fba4f-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="fba4f-107">此結構未定義于已發行的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="fba4f-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="fba4f-108">若要使用此結構，請使用所示的確切格式來定義它。</span><span class="sxs-lookup"><span data-stu-id="fba4f-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fba4f-109">語法</span><span class="sxs-lookup"><span data-stu-id="fba4f-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="fba4f-110">成員</span><span class="sxs-lookup"><span data-stu-id="fba4f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fba4f-111">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="fba4f-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="fba4f-112">包含次要屬性工作表之父系的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="fba4f-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="fba4f-113">**offsetTitle**</span><span class="sxs-lookup"><span data-stu-id="fba4f-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="fba4f-114">包含以位元組為單位的位移，從 **DSA \_ SEC \_ 頁面 \_ 資訊** 結構的開頭到以 Null 終止的 Unicode 字串，其中包含次要屬性工作表的標題。</span><span class="sxs-lookup"><span data-stu-id="fba4f-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="fba4f-115">**dsObjectNames**</span><span class="sxs-lookup"><span data-stu-id="fba4f-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="fba4f-116">包含定義次要屬性工作表的 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構。</span><span class="sxs-lookup"><span data-stu-id="fba4f-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="fba4f-117">一次只能建立一個次要屬性工作表，因此 **DSOBJECTNAMES** 結構只能包含一個 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。</span><span class="sxs-lookup"><span data-stu-id="fba4f-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fba4f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fba4f-118">Requirements</span></span>



| <span data-ttu-id="fba4f-119">需求</span><span class="sxs-lookup"><span data-stu-id="fba4f-119">Requirement</span></span> | <span data-ttu-id="fba4f-120">值</span><span class="sxs-lookup"><span data-stu-id="fba4f-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fba4f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fba4f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fba4f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fba4f-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fba4f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fba4f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fba4f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba4f-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fba4f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fba4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba4f-126">**WM \_ ADSPROP \_ 工作表 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="fba4f-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="fba4f-127">**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="fba4f-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="fba4f-128">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="fba4f-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="fba4f-129">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="fba4f-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





