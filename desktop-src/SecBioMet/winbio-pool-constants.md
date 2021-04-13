---
title: 'WINBIO_POOL 常數 (Winbio \_ 類型 .h) '
description: 指定要在會話中使用的生物特徵辨識單位集區類型。
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509407"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="ae9ec-103">WINBIO \_ 集區常數</span><span class="sxs-lookup"><span data-stu-id="ae9ec-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="ae9ec-104">下列常數可以用在 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 函式中，以指定要在會話中使用的生物特徵辨識單位集區類型。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="ae9ec-105">常數</span><span class="sxs-lookup"><span data-stu-id="ae9ec-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="ae9ec-106">描述</span><span class="sxs-lookup"><span data-stu-id="ae9ec-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="ae9ec-107"><dt>**WINBIO \_ 集區 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ec-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="ae9ec-108">集區類型未知。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="ae9ec-109"><dt>**WINBIO \_ 集區 \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ec-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="ae9ec-110">指定服務提供者所管理的生物特徵辨識單位共用集合。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="ae9ec-111"><dt>**WINBIO \_ 集區 \_ 私用**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ec-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="ae9ec-112">指定由呼叫端管理的生物特徵辨識單位集合。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="ae9ec-113"><dt>**\_未指派 WINBIO 集區 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ec-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="ae9ec-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="ae9ec-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae9ec-115">Requirements</span></span>



| <span data-ttu-id="ae9ec-116">需求</span><span class="sxs-lookup"><span data-stu-id="ae9ec-116">Requirement</span></span> | <span data-ttu-id="ae9ec-117">值</span><span class="sxs-lookup"><span data-stu-id="ae9ec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9ec-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae9ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9ec-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae9ec-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ae9ec-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae9ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9ec-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae9ec-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ae9ec-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ae9ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae9ec-123"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ae9ec-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9ec-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae9ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9ec-125">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="ae9ec-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





