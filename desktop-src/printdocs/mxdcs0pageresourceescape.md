---
description: MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ t 結構是 \_ \_ \_ 與 MXDC \_ XPS \_ S0PAGE \_ 資源 \_ t 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: 'MXDC_S0PAGE_RESOURCE_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192714"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="96e67-103">MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="96e67-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="96e67-104">**MXDC \_ S0PAGE \_ 資源 \_ ESCAPE \_ t** 結構是與 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ t**](mxdcxpss0pageresource.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。</span><span class="sxs-lookup"><span data-stu-id="96e67-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e67-105">語法</span><span class="sxs-lookup"><span data-stu-id="96e67-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="96e67-106">成員</span><span class="sxs-lookup"><span data-stu-id="96e67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96e67-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="96e67-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="96e67-108">[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員會設定為 MXDCOP \_ set \_ S0PAGE \_ RESOURCE。</span><span class="sxs-lookup"><span data-stu-id="96e67-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="96e67-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="96e67-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="96e67-110">XPS 檔頁面上代表資源的 [**MXDC \_ XPS \_ S0PAGE \_ 資源 \_ T**](mxdcxpss0pageresource.md) 結構，例如字型或影像檔案。</span><span class="sxs-lookup"><span data-stu-id="96e67-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96e67-111">備註</span><span class="sxs-lookup"><span data-stu-id="96e67-111">Remarks</span></span>

<span data-ttu-id="96e67-112">當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫該函式時，會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數中傳遞這個結構，而 [**MXDC \_ ESCAPE \_ 標頭 \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ SET \_ S0PAGE \_ 資源**。</span><span class="sxs-lookup"><span data-stu-id="96e67-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="96e67-113">結果是要傳送至 MXDC 的頁面資源。</span><span class="sxs-lookup"><span data-stu-id="96e67-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="96e67-114">配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。</span><span class="sxs-lookup"><span data-stu-id="96e67-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="96e67-115">呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間;不過，對 **StartPage** 和 **EndPage** 的呼叫之間可以有一個以上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="96e67-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="96e67-116">如果您針對頁面上的每個資源使用 **MXDCOP \_ set \_ S0PAGE \_ RESOURCE** **opCode** 來呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) ，然後再使用 **MXDCOP \_ set \_ S0PAGE\*\*\*\*opCode** 呼叫 **ExtEscape** ，串流耗用量就會更有效率。  </span><span class="sxs-lookup"><span data-stu-id="96e67-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e67-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="96e67-117">Requirements</span></span>



| <span data-ttu-id="96e67-118">需求</span><span class="sxs-lookup"><span data-stu-id="96e67-118">Requirement</span></span> | <span data-ttu-id="96e67-119">值</span><span class="sxs-lookup"><span data-stu-id="96e67-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="96e67-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96e67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96e67-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96e67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96e67-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96e67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96e67-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96e67-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96e67-124">標頭</span><span class="sxs-lookup"><span data-stu-id="96e67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e67-125"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="96e67-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e67-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96e67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e67-127">列印</span><span class="sxs-lookup"><span data-stu-id="96e67-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="96e67-128">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="96e67-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="96e67-129">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96e67-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="96e67-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="96e67-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="96e67-131">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="96e67-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

