---
description: CAPICOM \_ 匯出 \_ 旗標列舉型別會定義是否忽略任何私用金鑰匯出錯誤。
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: 'CAPICOM_EXPORT_FLAG 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990617"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="ed0ed-103">CAPICOM \_ 匯出 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="ed0ed-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="ed0ed-104">**CAPICOM \_ 匯出 \_ 旗** 標列舉型別會定義是否忽略任何私用金鑰匯出錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed0ed-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="ed0ed-105">成員</span><span class="sxs-lookup"><span data-stu-id="ed0ed-105">Members</span></span>



| <span data-ttu-id="ed0ed-106">member</span><span class="sxs-lookup"><span data-stu-id="ed0ed-106">Member</span></span>                                                            | <span data-ttu-id="ed0ed-107">描述</span><span class="sxs-lookup"><span data-stu-id="ed0ed-107">Description</span></span>                                               | <span data-ttu-id="ed0ed-108">值</span><span class="sxs-lookup"><span data-stu-id="ed0ed-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="ed0ed-109">**CAPICOM \_ 匯出 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="ed0ed-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="ed0ed-110">不會忽略任何私用金鑰匯出錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed0ed-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="ed0ed-111">0</span><span class="sxs-lookup"><span data-stu-id="ed0ed-111">0</span></span>     |
| <span data-ttu-id="ed0ed-112">**CAPICOM \_ 匯出 \_ 略 \_ 過 \_ 私密金鑰 \_ 不可 \_ 匯出的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="ed0ed-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="ed0ed-113">系統會忽略任何私用金鑰匯出錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed0ed-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="ed0ed-114">1</span><span class="sxs-lookup"><span data-stu-id="ed0ed-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="ed0ed-115">備註</span><span class="sxs-lookup"><span data-stu-id="ed0ed-115">Remarks</span></span>

<span data-ttu-id="ed0ed-116">\_ \_ 下列方法會使用 CAPICOM 匯出旗標列舉類型：</span><span class="sxs-lookup"><span data-stu-id="ed0ed-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="ed0ed-117">**憑證。儲存**</span><span class="sxs-lookup"><span data-stu-id="ed0ed-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="ed0ed-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed0ed-118">Requirements</span></span>



| <span data-ttu-id="ed0ed-119">需求</span><span class="sxs-lookup"><span data-stu-id="ed0ed-119">Requirement</span></span> | <span data-ttu-id="ed0ed-120">值</span><span class="sxs-lookup"><span data-stu-id="ed0ed-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0ed-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ed0ed-121">Redistributable</span></span><br/> | <span data-ttu-id="ed0ed-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ed0ed-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="ed0ed-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ed0ed-123">Header</span></span><br/>          | <dl> <span data-ttu-id="ed0ed-124"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ed-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




