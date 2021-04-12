---
description: MXDC \_ S0PAGE \_ 傳遞 \_ escape \_ t 結構是 \_ \_ \_ 與 MXDC \_ S0PAGE \_ 資料 \_ T 結構串連的 MXDC ESCAPE HEADER t 結構。
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: 'MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319571"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="15b31-103">MXDC \_ S0PAGE \_ 傳遞 \_ ESCAPE \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="15b31-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="15b31-104">**MXDC \_ S0PAGE \_ 傳遞 \_ escape \_ t** 結構是與 [**MXDC \_ S0PAGE \_ 資料 \_ T**](mxdcs0pagedata.md)結構串連的 [**MXDC \_ ESCAPE \_ HEADER \_ t**](mxdcescapeheader.md)結構。</span><span class="sxs-lookup"><span data-stu-id="15b31-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b31-105">語法</span><span class="sxs-lookup"><span data-stu-id="15b31-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="15b31-106">成員</span><span class="sxs-lookup"><span data-stu-id="15b31-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15b31-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="15b31-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="15b31-108">[**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構，其 **opCode** 成員會設定為 **MXDCOP \_ set \_ S0PAGE**。</span><span class="sxs-lookup"><span data-stu-id="15b31-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="15b31-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="15b31-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="15b31-110">代表 XPS 檔頁面的 [**MxdcS0PageData**](mxdcs0pagedata.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="15b31-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15b31-111">備註</span><span class="sxs-lookup"><span data-stu-id="15b31-111">Remarks</span></span>

<span data-ttu-id="15b31-112">當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 來呼叫時，這個結構會在 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函數的 *LpszInData* 參數中傳遞，而 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構的 **opCode** 成員是 **MXDCOP \_ SET \_ S0PAGE**。</span><span class="sxs-lookup"><span data-stu-id="15b31-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="15b31-113">結果是 Microsoft XML 檔轉換器 (MXDC) 會將頁面傳送至印表機，而不需要處理。</span><span class="sxs-lookup"><span data-stu-id="15b31-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="15b31-114">配置如下所示之 escape 的記憶體，視需要設定欄位，然後呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)。</span><span class="sxs-lookup"><span data-stu-id="15b31-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="15b31-115">呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間。</span><span class="sxs-lookup"><span data-stu-id="15b31-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="15b31-116">呼叫應用程式負責驗證 XPS 檔頁面的 XML。</span><span class="sxs-lookup"><span data-stu-id="15b31-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="15b31-117">如果您在使用 **MXDCOP \_ set \_ S0PAGE** 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，將 **MXDCOP \_ 設定 \_ S0PAGE \_ 資源** 作為頁面上每個資源的 **opCode** ，則串流耗用量會更有效率。</span><span class="sxs-lookup"><span data-stu-id="15b31-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b31-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="15b31-118">Requirements</span></span>



| <span data-ttu-id="15b31-119">需求</span><span class="sxs-lookup"><span data-stu-id="15b31-119">Requirement</span></span> | <span data-ttu-id="15b31-120">值</span><span class="sxs-lookup"><span data-stu-id="15b31-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="15b31-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15b31-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15b31-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15b31-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15b31-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15b31-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15b31-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15b31-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="15b31-125">標頭</span><span class="sxs-lookup"><span data-stu-id="15b31-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b31-126"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="15b31-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15b31-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15b31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b31-128">列印</span><span class="sxs-lookup"><span data-stu-id="15b31-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="15b31-129">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="15b31-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="15b31-130">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15b31-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="15b31-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="15b31-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="15b31-132">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="15b31-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

