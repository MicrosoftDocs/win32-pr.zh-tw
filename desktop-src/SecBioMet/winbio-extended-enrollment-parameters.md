---
title: 'WINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構 (Winbio \_ adapter .h) '
description: 包含引擎介面卡建立註冊範本時所需的其他資訊。
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464608"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="e53c5-105">WINBIO \_ 延伸 \_ 註冊 \_ 參數結構</span><span class="sxs-lookup"><span data-stu-id="e53c5-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="e53c5-106">**WINBIO \_ 延伸 \_ 註冊 \_ 參數** 結構包含引擎介面卡建立註冊範本時所需的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e53c5-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53c5-107">語法</span><span class="sxs-lookup"><span data-stu-id="e53c5-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="e53c5-108">成員</span><span class="sxs-lookup"><span data-stu-id="e53c5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e53c5-109">**大小**</span><span class="sxs-lookup"><span data-stu-id="e53c5-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e53c5-110">**WINBIO \_ 延伸 \_ 註冊 \_ 參數** 結構的大小 (以位元組為單位) 。</span><span class="sxs-lookup"><span data-stu-id="e53c5-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e53c5-111">**SubFactor**</span><span class="sxs-lookup"><span data-stu-id="e53c5-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="e53c5-112">其中一個 [**WINBIO \_ 生物特徵辨識 \_ 子類型常數**](winbio-biometric-subtype-constants.md) 值，可提供註冊的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e53c5-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e53c5-113">備註</span><span class="sxs-lookup"><span data-stu-id="e53c5-113">Remarks</span></span>

<span data-ttu-id="e53c5-114">Windows 生物特徵辨識架構在註冊作業期間，將此結構傳遞給 [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) 方法。</span><span class="sxs-lookup"><span data-stu-id="e53c5-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53c5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e53c5-115">Requirements</span></span>



| <span data-ttu-id="e53c5-116">需求</span><span class="sxs-lookup"><span data-stu-id="e53c5-116">Requirement</span></span> | <span data-ttu-id="e53c5-117">值</span><span class="sxs-lookup"><span data-stu-id="e53c5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e53c5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e53c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e53c5-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e53c5-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="e53c5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e53c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e53c5-121">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e53c5-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="e53c5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e53c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e53c5-123"><dt>Winbio \_ adapter .h (包括 Winbio \_ adapter .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e53c5-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





