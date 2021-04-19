---
description: 定義輸出保護管理員 (OPM) 的狀態。
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982797"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="792ff-103">MF \_ 媒體 \_ 引擎 \_ OPM \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="792ff-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="792ff-104">定義 [輸出保護管理員](output-protection-manager.md) (OPM) 的狀態。</span><span class="sxs-lookup"><span data-stu-id="792ff-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="792ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="792ff-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="792ff-106">常數</span><span class="sxs-lookup"><span data-stu-id="792ff-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="792ff-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_ \_ \_ \_ 未要求 MF 媒體引擎 \_ OPM**</span><span class="sxs-lookup"><span data-stu-id="792ff-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-108">預設狀態。</span><span class="sxs-lookup"><span data-stu-id="792ff-108">Default status.</span></span> <span data-ttu-id="792ff-109">當內容未受保護時，用來傳回正確的狀態。</span><span class="sxs-lookup"><span data-stu-id="792ff-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="792ff-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**已 \_ 建立 MF 媒體 \_ 引擎 \_ OPM \_**</span><span class="sxs-lookup"><span data-stu-id="792ff-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-111">已成功建立 OPM。</span><span class="sxs-lookup"><span data-stu-id="792ff-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="792ff-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗的 \_ VM**</span><span class="sxs-lookup"><span data-stu-id="792ff-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-113">OPM 失敗，因為在虛擬 (VM) 中執行。</span><span class="sxs-lookup"><span data-stu-id="792ff-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="792ff-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗 \_ BDA**</span><span class="sxs-lookup"><span data-stu-id="792ff-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-115">OPM 失敗，因為沒有圖形驅動程式，且系統正在使用基本的顯示器介面卡 (BDA) 。</span><span class="sxs-lookup"><span data-stu-id="792ff-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="792ff-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗的 \_ 未簽署 \_ 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="792ff-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-117">OPM 失敗，因為圖形驅動程式未經過 PE 簽署，因此切換回變形。</span><span class="sxs-lookup"><span data-stu-id="792ff-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="792ff-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="792ff-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="792ff-119">OPM 因其他原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="792ff-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="792ff-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="792ff-120">Requirements</span></span>



| <span data-ttu-id="792ff-121">需求</span><span class="sxs-lookup"><span data-stu-id="792ff-121">Requirement</span></span> | <span data-ttu-id="792ff-122">值</span><span class="sxs-lookup"><span data-stu-id="792ff-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="792ff-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="792ff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="792ff-124">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="792ff-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="792ff-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="792ff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="792ff-126">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="792ff-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="792ff-127">Idl</span><span class="sxs-lookup"><span data-stu-id="792ff-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="792ff-128"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="792ff-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792ff-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="792ff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792ff-130">媒體基礎列舉</span><span class="sxs-lookup"><span data-stu-id="792ff-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




