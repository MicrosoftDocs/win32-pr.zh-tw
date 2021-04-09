---
title: 'WINBIO_CREDENTIAL_TYPE 列舉 (Winbio \_ 類型 .h) '
description: 定義可以用來篩選認證類型的旗標。
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE 列舉 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844320"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="78049-104">WINBIO \_ 認證 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="78049-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="78049-105">定義可以用來篩選認證類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="78049-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="78049-106">[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)、 [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)和 [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)函式會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="78049-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="78049-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78049-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="78049-108">常數</span><span class="sxs-lookup"><span data-stu-id="78049-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="78049-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO \_ 認證 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="78049-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="78049-110">篩選密碼認證。</span><span class="sxs-lookup"><span data-stu-id="78049-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="78049-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ 認證 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="78049-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="78049-112">篩選所有認證。</span><span class="sxs-lookup"><span data-stu-id="78049-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78049-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="78049-113">Requirements</span></span>



| <span data-ttu-id="78049-114">需求</span><span class="sxs-lookup"><span data-stu-id="78049-114">Requirement</span></span> | <span data-ttu-id="78049-115">值</span><span class="sxs-lookup"><span data-stu-id="78049-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78049-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78049-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78049-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78049-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="78049-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78049-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78049-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78049-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="78049-120">標頭</span><span class="sxs-lookup"><span data-stu-id="78049-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78049-121"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="78049-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78049-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78049-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78049-123">用戶端應用程式列舉</span><span class="sxs-lookup"><span data-stu-id="78049-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="78049-124">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="78049-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="78049-125">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="78049-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="78049-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="78049-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





