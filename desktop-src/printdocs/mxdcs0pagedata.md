---
description: MXDC \_ S0PAGE \_ DATA \_ T 結構會保存 XPS 檔頁面，以傳遞至 Microsoft xps 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: 'MXDC_S0PAGE_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693803"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="50fba-103">MXDC \_ S0PAGE \_ 資料 \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="50fba-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="50fba-104">**MXDC \_ S0PAGE \_ DATA \_ T** 結構會保存 XPS 檔頁面，以傳遞至 MICROSOFT xps 檔轉換器 (MXDC) 輸出檔，而不需要任何處理。</span><span class="sxs-lookup"><span data-stu-id="50fba-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="50fba-105">語法</span><span class="sxs-lookup"><span data-stu-id="50fba-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="50fba-106">成員</span><span class="sxs-lookup"><span data-stu-id="50fba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="50fba-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="50fba-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="50fba-108">輸出緩衝區的大小（ **bData**）。</span><span class="sxs-lookup"><span data-stu-id="50fba-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="50fba-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="50fba-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="50fba-110">XPS 檔頁面。</span><span class="sxs-lookup"><span data-stu-id="50fba-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50fba-111">備註</span><span class="sxs-lookup"><span data-stu-id="50fba-111">Remarks</span></span>

<span data-ttu-id="50fba-112">此結構會附加至 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md) 結構， (其 **opCode** 設定為 MXDCOP \_ set \_ S0PAGE) ，以建立 [**MXDC \_ S0PAGE \_ 通過 \_ ESCAPE \_ T**](mxdcs0pagepassthroughescape.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="50fba-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="50fba-113">該結構接著會傳遞至 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)函式的 *lpszInData* 參數，並以 [**MXDC \_ escape**](mxdc-escape.md)作為 ESCAPE 來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="50fba-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="50fba-114">結果是 MXDC 會將頁面傳遞至輸出，而不進行處理。</span><span class="sxs-lookup"><span data-stu-id="50fba-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="50fba-115">呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) 必須介於對 [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) 的呼叫與對 [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)的呼叫之間。</span><span class="sxs-lookup"><span data-stu-id="50fba-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="50fba-116">呼叫應用程式負責驗證 XPS 檔頁面的 XML。</span><span class="sxs-lookup"><span data-stu-id="50fba-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="50fba-117">如果您在使用 **MXDCOP \_ set \_ S0PAGE** 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，將 **MXDCOP \_ 設定 \_ S0PAGE \_ 資源** 作為頁面上每個資源的 **opCode** ，則串流耗用量會更有效率。</span><span class="sxs-lookup"><span data-stu-id="50fba-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="50fba-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="50fba-118">Requirements</span></span>



| <span data-ttu-id="50fba-119">需求</span><span class="sxs-lookup"><span data-stu-id="50fba-119">Requirement</span></span> | <span data-ttu-id="50fba-120">值</span><span class="sxs-lookup"><span data-stu-id="50fba-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="50fba-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50fba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="50fba-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fba-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50fba-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50fba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="50fba-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fba-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50fba-125">標頭</span><span class="sxs-lookup"><span data-stu-id="50fba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fba-126"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="50fba-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50fba-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50fba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fba-128">列印</span><span class="sxs-lookup"><span data-stu-id="50fba-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="50fba-129">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="50fba-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="50fba-130">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50fba-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="50fba-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="50fba-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="50fba-132">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="50fba-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

