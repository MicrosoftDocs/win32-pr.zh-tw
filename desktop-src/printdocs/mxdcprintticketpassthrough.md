---
description: MXDC 的 \_ PRINTTICKET \_ 資料 \_ T 結構會保存 XPS 檔列印票證，其中包含的印表機和列印工作設定，可傳遞給 Microsoft XPS 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: 'MXDC_PRINTTICKET_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849212"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="f6957-103">MXDC \_ PRINTTICKET \_ 資料 \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="f6957-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="f6957-104">**MXDC 的 \_ PRINTTICKET \_ 資料 \_ T** 結構會保存 XPS 檔列印票證，其中包含的印表機和列印工作設定，可傳遞給 MICROSOFT XPS 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。</span><span class="sxs-lookup"><span data-stu-id="f6957-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6957-105">語法</span><span class="sxs-lookup"><span data-stu-id="f6957-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="f6957-106">成員</span><span class="sxs-lookup"><span data-stu-id="f6957-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6957-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="f6957-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="f6957-108">列印票證的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6957-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f6957-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="f6957-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="f6957-110">XPS 檔列印票證。</span><span class="sxs-lookup"><span data-stu-id="f6957-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6957-111">備註</span><span class="sxs-lookup"><span data-stu-id="f6957-111">Remarks</span></span>

<span data-ttu-id="f6957-112">此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md) 結構，此結構的 **opCode** 成員設定為 **MXDCOP \_ Printticket \_ fixed \_ PAGE**、 **MXDCOP \_ PRINTTICKET \_ fixed \_ doc** 或 **MXDCOP \_ PRINTTICKET 固定檔 \_ \_ \_ SEQ** ，以建立 MXDC 的 [**\_ printticket \_ ESCAPE \_ T**](mxdcprintticketescape.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f6957-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="f6957-113">**MXDC 的 \_ PRINTTICKET \_ escape \_ T** 結構接著會在使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫時，傳遞給 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數。</span><span class="sxs-lookup"><span data-stu-id="f6957-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="f6957-114">效果是將列印票證寫入至 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="f6957-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="f6957-115">如果作業 **碼** 設定為 **MXDCOP 的 \_ PRINTTICKET \_ 固定 \_ 頁面**，則對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間必須發生 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f6957-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="f6957-116">如果 **opCode** 設定為 **MXDCOP \_ Printticket \_ 固定 \_** 檔或 **MXDCOP \_ printticket 固定檔 \_ \_ \_ SEQ**，則在呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)與 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)的呼叫之間必須進行 **ExtEscape** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f6957-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6957-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6957-117">Requirements</span></span>



| <span data-ttu-id="f6957-118">需求</span><span class="sxs-lookup"><span data-stu-id="f6957-118">Requirement</span></span> | <span data-ttu-id="f6957-119">值</span><span class="sxs-lookup"><span data-stu-id="f6957-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f6957-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6957-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f6957-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6957-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6957-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6957-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f6957-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6957-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6957-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f6957-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6957-125"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6957-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6957-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6957-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6957-127">列印</span><span class="sxs-lookup"><span data-stu-id="f6957-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f6957-128">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="f6957-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="f6957-129">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6957-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6957-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="f6957-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="f6957-131">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="f6957-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

