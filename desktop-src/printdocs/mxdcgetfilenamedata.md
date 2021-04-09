---
description: MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T 結構會保存 Microsoft XPS 檔轉換器的完整路徑和檔案名， (MXDC) 輸出檔。
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: 'MXDC_GET_FILENAME_DATA_T 結構 (Mxdc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849213"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="c0ac8-103">MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T 結構</span><span class="sxs-lookup"><span data-stu-id="c0ac8-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="c0ac8-104">**MXDC \_ 取得 \_ 檔案名 \_ 資料 \_ T** 結構會保存 Microsoft XPS 檔轉換器的完整路徑和檔案名， (MXDC) 輸出檔。</span><span class="sxs-lookup"><span data-stu-id="c0ac8-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ac8-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0ac8-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="c0ac8-106">成員</span><span class="sxs-lookup"><span data-stu-id="c0ac8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0ac8-107">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="c0ac8-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="c0ac8-108">輸出緩衝區的大小（ **wszData**）。</span><span class="sxs-lookup"><span data-stu-id="c0ac8-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="c0ac8-109">**wszData**</span><span class="sxs-lookup"><span data-stu-id="c0ac8-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="c0ac8-110">輸出檔的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="c0ac8-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0ac8-111">備註</span><span class="sxs-lookup"><span data-stu-id="c0ac8-111">Remarks</span></span>

<span data-ttu-id="c0ac8-112">當使用 [**MXDC \_ escape**](mxdc-escape.md) escape 呼叫 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)時，會傳回這個結構，而且在 *lpszInData* 參數中傳遞的 [**MXDC \_ ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md)結構會將其 **opCode** 設定為 **MXDCOP \_ 取得 \_ 檔案名**。</span><span class="sxs-lookup"><span data-stu-id="c0ac8-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ac8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0ac8-113">Requirements</span></span>



| <span data-ttu-id="c0ac8-114">需求</span><span class="sxs-lookup"><span data-stu-id="c0ac8-114">Requirement</span></span> | <span data-ttu-id="c0ac8-115">值</span><span class="sxs-lookup"><span data-stu-id="c0ac8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c0ac8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0ac8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ac8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0ac8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0ac8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0ac8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ac8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0ac8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0ac8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c0ac8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ac8-121"><dt>Mxdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ac8-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ac8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0ac8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ac8-123">列印</span><span class="sxs-lookup"><span data-stu-id="c0ac8-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c0ac8-124">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="c0ac8-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="c0ac8-125">[GDI 印表機 Escape 函式](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0ac8-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0ac8-126">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="c0ac8-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="c0ac8-127">**MXDC \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="c0ac8-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

