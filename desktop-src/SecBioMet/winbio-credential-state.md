---
title: 'WINBIO_CREDENTIAL_STATE 列舉 (Winbio \_ 類型 .h) '
description: 定義值，這個值會指定認證是否已與終端使用者的生物特徵辨識資料相關聯。
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE 列舉 Windows 生物特徵辨識架構 API
- PWINBIO_CREDENTIAL_STATE 列舉指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317147"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="73d84-105">WINBIO \_ 認證 \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="73d84-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="73d84-106">定義值，這個值會指定認證是否已與終端使用者的生物特徵辨識資料相關聯。</span><span class="sxs-lookup"><span data-stu-id="73d84-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="73d84-107">[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)函數會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="73d84-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d84-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73d84-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="73d84-109">常數</span><span class="sxs-lookup"><span data-stu-id="73d84-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73d84-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_ \_ 未設定 WINBIO \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="73d84-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="73d84-111">認證已與終端使用者建立關聯。</span><span class="sxs-lookup"><span data-stu-id="73d84-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="73d84-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO \_ 認證 \_ 集**</span><span class="sxs-lookup"><span data-stu-id="73d84-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="73d84-113">認證尚未與終端使用者建立關聯。</span><span class="sxs-lookup"><span data-stu-id="73d84-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73d84-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="73d84-114">Requirements</span></span>



| <span data-ttu-id="73d84-115">需求</span><span class="sxs-lookup"><span data-stu-id="73d84-115">Requirement</span></span> | <span data-ttu-id="73d84-116">值</span><span class="sxs-lookup"><span data-stu-id="73d84-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d84-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73d84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73d84-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73d84-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="73d84-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73d84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73d84-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73d84-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="73d84-121">標頭</span><span class="sxs-lookup"><span data-stu-id="73d84-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73d84-122"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="73d84-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d84-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73d84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d84-124">用戶端應用程式列舉</span><span class="sxs-lookup"><span data-stu-id="73d84-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="73d84-125">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="73d84-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





