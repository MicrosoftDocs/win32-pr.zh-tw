---
title: 'WINBIO_BIR_QUALITY 常數 (Winbio \_ 類型 .h) '
description: 如果未指定0到100的整數值，請指定 BIR 中生物特徵辨識資料的相對品質。
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106193"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="1ef76-103">WINBIO \_ BIR \_ 品質常數</span><span class="sxs-lookup"><span data-stu-id="1ef76-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="1ef76-104">[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **DataQuality** 成員會使用下列旗標，以指定從0到100的整數值未指定時，BIR 中生物特徵辨識資料的相對品質。</span><span class="sxs-lookup"><span data-stu-id="1ef76-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="1ef76-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="1ef76-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1ef76-106">Description</span><span class="sxs-lookup"><span data-stu-id="1ef76-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="1ef76-107"><dt>**WINBIO \_資料 \_ 品質 \_ 未 \_ 設定**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="1ef76-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="1ef76-108">BIR 建立者支援品質度量，但未在 BIR 中設定任何值。</span><span class="sxs-lookup"><span data-stu-id="1ef76-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="1ef76-109"><dt>**WINBIO \_\_ \_ 不 \_ 支援資料品質**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ef76-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="1ef76-110">BIR 建立者不支援品質度量。</span><span class="sxs-lookup"><span data-stu-id="1ef76-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="1ef76-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ef76-111">Requirements</span></span>



| <span data-ttu-id="1ef76-112">需求</span><span class="sxs-lookup"><span data-stu-id="1ef76-112">Requirement</span></span> | <span data-ttu-id="1ef76-113">值</span><span class="sxs-lookup"><span data-stu-id="1ef76-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef76-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ef76-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef76-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef76-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1ef76-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ef76-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef76-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef76-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1ef76-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1ef76-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef76-119"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1ef76-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef76-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ef76-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef76-121">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="1ef76-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





