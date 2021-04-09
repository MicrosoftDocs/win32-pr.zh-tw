---
description: MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T 結構會保存與 XPS 檔頁面相關聯的資源（例如影像或字型）相關資訊，並將其傳遞至 Microsoft XPS 檔轉換器 (MXDC) 輸出檔。
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: 'MXDC_XPS_S0PAGE_RESOURCE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849755"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="8425f-103">MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="8425f-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="8425f-104">**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T** 結構會保存與 XPS 檔頁面相關聯的資源（例如影像或字型）相關資訊，並將其傳遞至 Microsoft xps 檔轉換器 (MXDC) 輸出檔。</span><span class="sxs-lookup"><span data-stu-id="8425f-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8425f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8425f-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="8425f-106">成員</span><span class="sxs-lookup"><span data-stu-id="8425f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8425f-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8425f-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8425f-108">此結構和其指向的資源的總大小。</span><span class="sxs-lookup"><span data-stu-id="8425f-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="8425f-109">**dwResourceType**</span><span class="sxs-lookup"><span data-stu-id="8425f-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="8425f-110">[**MXDC \_ S0 \_ 頁面 \_**](mxdcs0pageenums.md)列舉類型的值，指出資源的類型，例如 TIFF 影像或 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="8425f-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="8425f-111">**szUri**</span><span class="sxs-lookup"><span data-stu-id="8425f-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="8425f-112">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="8425f-112">The URI of the resource.</span></span> <span data-ttu-id="8425f-113">這不能超過260個位元組。</span><span class="sxs-lookup"><span data-stu-id="8425f-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8425f-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="8425f-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="8425f-115">資源的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8425f-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8425f-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="8425f-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="8425f-117">資源的資料，大小為 1 + 資源大小的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="8425f-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8425f-118">備註</span><span class="sxs-lookup"><span data-stu-id="8425f-118">Remarks</span></span>

<span data-ttu-id="8425f-119">此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md) 結構 (，其作業 **碼** 設定為 **MXDCOP \_ set \_ S0PAGERESOURCE**) 以建立 [**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T**](mxdcs0pageresourceescape.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="8425f-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="8425f-120">產生的 **MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T** 結構接著會傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數，並使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="8425f-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="8425f-121">效果是將資源傳送至 MXDC 進行轉換，並寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="8425f-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="8425f-122">呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間;不過，對 **StartPage** 和 **EndPage** 的呼叫之間可以有一個以上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8425f-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="8425f-123">如果您針對頁面上的每個資源使用 **MXDCOP \_ set \_ S0PAGE \_ RESOURCE** **opCode** 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) ，然後再使用 **MXDCOP \_ set \_ S0PAGE** **opCode** 呼叫 **ExtEscape** ，串流耗用量就會更有效率。</span><span class="sxs-lookup"><span data-stu-id="8425f-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8425f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8425f-124">Requirements</span></span>



| <span data-ttu-id="8425f-125">需求</span><span class="sxs-lookup"><span data-stu-id="8425f-125">Requirement</span></span> | <span data-ttu-id="8425f-126">值</span><span class="sxs-lookup"><span data-stu-id="8425f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8425f-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8425f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8425f-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8425f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8425f-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8425f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8425f-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8425f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8425f-131">標頭</span><span class="sxs-lookup"><span data-stu-id="8425f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8425f-132"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="8425f-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8425f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8425f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8425f-134">列印</span><span class="sxs-lookup"><span data-stu-id="8425f-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8425f-135">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="8425f-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="8425f-136">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8425f-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8425f-137">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="8425f-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="8425f-138">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="8425f-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

