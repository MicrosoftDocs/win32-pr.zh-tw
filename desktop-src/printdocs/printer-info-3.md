---
description: 印表機 \_ 資訊 \_ 3 結構會指定印表機安全性資訊。
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: 'PRINTER_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998144"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="d1839-103">印表機 \_ 資訊 \_ 3 結構</span><span class="sxs-lookup"><span data-stu-id="d1839-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="d1839-104">**印表機 \_ 資訊 \_ 3** 結構會指定印表機安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="d1839-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1839-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1839-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="d1839-106">成員</span><span class="sxs-lookup"><span data-stu-id="d1839-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1839-107">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d1839-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="d1839-108">[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構的指標，指定印表機的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="d1839-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1839-109">備註</span><span class="sxs-lookup"><span data-stu-id="d1839-109">Remarks</span></span>

<span data-ttu-id="d1839-110">**印表機 \_ 資訊 \_ 3** 結構可讓應用程式取得和設定印表機的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d1839-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="d1839-111">即使它缺少特定的印表機權限，呼叫者仍可能這麼做，只要它具有 [**SetPrinter**](setprinter.md) 和 [**GetPrinter**](getprinter.md)中所述的標準許可權即可。</span><span class="sxs-lookup"><span data-stu-id="d1839-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="d1839-112">因此，應用程式可能會暫時拒絕印表機的所有存取，同時允許印表機的擁有者存取印表機的任意 ACL。</span><span class="sxs-lookup"><span data-stu-id="d1839-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1839-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1839-113">Requirements</span></span>



| <span data-ttu-id="d1839-114">需求</span><span class="sxs-lookup"><span data-stu-id="d1839-114">Requirement</span></span> | <span data-ttu-id="d1839-115">值</span><span class="sxs-lookup"><span data-stu-id="d1839-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1839-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1839-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1839-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1839-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d1839-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1839-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1839-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1839-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d1839-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d1839-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1839-121"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d1839-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1839-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1839-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1839-123">列印</span><span class="sxs-lookup"><span data-stu-id="d1839-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d1839-124">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="d1839-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d1839-125">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d1839-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="d1839-126">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d1839-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="d1839-127">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d1839-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="d1839-128">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d1839-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="d1839-129">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d1839-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="d1839-130">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="d1839-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

