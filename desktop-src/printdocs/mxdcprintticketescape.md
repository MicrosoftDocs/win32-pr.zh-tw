---
description: MXDC \_ 的 printticket \_ escape \_ t 結構是 \_ \_ \_ 與 MXDC 的 \_ printticket \_ 資料 \_ t 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: 'MXDC_PRINTTICKET_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982721"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="2ce56-103">MXDC \_ PRINTTICKET \_ ESCAPE \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="2ce56-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="2ce56-104">**MXDC 的 \_ printticket \_ escape \_ t** 結構是與 [**MXDC 的 \_ printticket \_ 資料 \_ t**](mxdcprintticketpassthrough.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。</span><span class="sxs-lookup"><span data-stu-id="2ce56-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce56-105">語法</span><span class="sxs-lookup"><span data-stu-id="2ce56-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="2ce56-106">成員</span><span class="sxs-lookup"><span data-stu-id="2ce56-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ce56-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="2ce56-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="2ce56-108">[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員設定為 MXDCOP \_ PRINTTICKET \_ 固定 \_ 頁面、MXDCOP \_ PRINTTICKET 固定檔 \_ \_ 或 MXDCOP \_ PRINTTICKET 固定檔 \_ \_ \_ SEQ。</span><span class="sxs-lookup"><span data-stu-id="2ce56-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="2ce56-109">**printTicketData**</span><span class="sxs-lookup"><span data-stu-id="2ce56-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="2ce56-110">包含列印票證的 [**MXDC \_ PRINTTICKET \_ 資料 \_ T**](mxdcprintticketpassthrough.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2ce56-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ce56-111">備註</span><span class="sxs-lookup"><span data-stu-id="2ce56-111">Remarks</span></span>

<span data-ttu-id="2ce56-112">當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫該函式，而 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ printticket \_ fixed \_ PAGE**、 **MXDCOP \_ printticket \_ fixed \_ doc** 或 **MXDCOP \_ printticket \_ 固定檔 \_ \_ SEQ** 時，此結構會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *lpszInData* 參數中傳遞。</span><span class="sxs-lookup"><span data-stu-id="2ce56-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="2ce56-113">結果是將列印票證寫入至 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="2ce56-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="2ce56-114">配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。</span><span class="sxs-lookup"><span data-stu-id="2ce56-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="2ce56-115">如果作業 **碼** 設定為 **MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**，則對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須發生 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="2ce56-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="2ce56-116">如果 **opCode** 設定為 **MXDCOP \_ Printticket \_ 固定 \_** 檔或 **MXDCOP \_ printticket 固定檔 \_ \_ \_ SEQ**，則在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)與 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間必須進行 **ExtEscape** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="2ce56-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce56-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ce56-117">Requirements</span></span>



| <span data-ttu-id="2ce56-118">需求</span><span class="sxs-lookup"><span data-stu-id="2ce56-118">Requirement</span></span> | <span data-ttu-id="2ce56-119">值</span><span class="sxs-lookup"><span data-stu-id="2ce56-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2ce56-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ce56-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce56-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ce56-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ce56-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ce56-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce56-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ce56-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ce56-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2ce56-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ce56-125"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce56-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce56-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ce56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce56-127">列印</span><span class="sxs-lookup"><span data-stu-id="2ce56-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2ce56-128">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="2ce56-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="2ce56-129">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ce56-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2ce56-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="2ce56-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="2ce56-131">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="2ce56-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

