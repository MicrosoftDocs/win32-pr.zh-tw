---
description: 印表機 \_ 列舉 \_ 值結構會指定 EnumPrinterDataEx 函數所傳回之印表機設定值的值名稱、類型和資料。
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: 'PRINTER_ENUM_VALUES 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974507"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="e18d2-103">印表機 \_ 列舉 \_ 值結構</span><span class="sxs-lookup"><span data-stu-id="e18d2-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="e18d2-104">**印表機 \_ 列舉 \_ 值** 結構會指定 [**EnumPrinterDataEx**](enumprinterdataex.md)函數所傳回之印表機設定值的值名稱、類型和資料。</span><span class="sxs-lookup"><span data-stu-id="e18d2-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="e18d2-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="e18d2-106">成員</span><span class="sxs-lookup"><span data-stu-id="e18d2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e18d2-107">**pValueName**</span><span class="sxs-lookup"><span data-stu-id="e18d2-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="e18d2-108">以 null 結束的字串指標，指定抓取值的名稱。</span><span class="sxs-lookup"><span data-stu-id="e18d2-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="e18d2-109">**cbValueName**</span><span class="sxs-lookup"><span data-stu-id="e18d2-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="e18d2-110">**PValueName** 成員中的位元組數目，包括結束的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="e18d2-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="e18d2-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="e18d2-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="e18d2-112">表示 **.pdata** 成員所指向之資料類型的代碼。</span><span class="sxs-lookup"><span data-stu-id="e18d2-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="e18d2-113">如需可能的類型代碼清單，請參閱登錄 [數值型別](/windows/desktop/SysInfo/registry-value-types)。</span><span class="sxs-lookup"><span data-stu-id="e18d2-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="e18d2-114">**.Pdata**</span><span class="sxs-lookup"><span data-stu-id="e18d2-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="e18d2-115">緩衝區的指標，其中包含抓取值的資料。</span><span class="sxs-lookup"><span data-stu-id="e18d2-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="e18d2-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="e18d2-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="e18d2-117">在 **.pdata** 緩衝區中取出的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e18d2-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e18d2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e18d2-118">Requirements</span></span>



| <span data-ttu-id="e18d2-119">需求</span><span class="sxs-lookup"><span data-stu-id="e18d2-119">Requirement</span></span> | <span data-ttu-id="e18d2-120">值</span><span class="sxs-lookup"><span data-stu-id="e18d2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18d2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e18d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e18d2-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e18d2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e18d2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e18d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e18d2-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e18d2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e18d2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e18d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18d2-126"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e18d2-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e18d2-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e18d2-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e18d2-128">**\_ 印表機 \_ 列舉 \_ VALUESW** (Unicode) 和 **\_ 印表機 \_ 列舉 \_ VALUESA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e18d2-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e18d2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e18d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18d2-130">列印</span><span class="sxs-lookup"><span data-stu-id="e18d2-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e18d2-131">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="e18d2-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e18d2-132">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="e18d2-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

