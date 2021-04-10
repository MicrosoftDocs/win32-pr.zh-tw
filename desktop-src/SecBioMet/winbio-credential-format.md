---
title: 'WINBIO_CREDENTIAL_FORMAT 列舉 (Winbio \_ 類型 .h) '
description: 定義可以用來指定使用者認證格式的旗標。
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT 列舉 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103697"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="02cd1-104">WINBIO \_ 認證 \_ 格式列舉</span><span class="sxs-lookup"><span data-stu-id="02cd1-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="02cd1-105">定義可以用來指定使用者認證格式的旗標。</span><span class="sxs-lookup"><span data-stu-id="02cd1-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="02cd1-106">[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)函數會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="02cd1-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cd1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02cd1-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="02cd1-108">常數</span><span class="sxs-lookup"><span data-stu-id="02cd1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="02cd1-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ 密碼 \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="02cd1-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="02cd1-110">密碼採用一般格式。</span><span class="sxs-lookup"><span data-stu-id="02cd1-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="02cd1-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO 的 \_ 密碼已 \_ 壓縮**</span><span class="sxs-lookup"><span data-stu-id="02cd1-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="02cd1-112">密碼是壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="02cd1-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="02cd1-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ 密碼 \_ 受保護**</span><span class="sxs-lookup"><span data-stu-id="02cd1-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="02cd1-114">密碼認證已使用 [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta)包裝。</span><span class="sxs-lookup"><span data-stu-id="02cd1-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02cd1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02cd1-115">Requirements</span></span>



| <span data-ttu-id="02cd1-116">需求</span><span class="sxs-lookup"><span data-stu-id="02cd1-116">Requirement</span></span> | <span data-ttu-id="02cd1-117">值</span><span class="sxs-lookup"><span data-stu-id="02cd1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02cd1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02cd1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02cd1-119">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02cd1-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="02cd1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02cd1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02cd1-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02cd1-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="02cd1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="02cd1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02cd1-123"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="02cd1-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02cd1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02cd1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cd1-125">用戶端應用程式列舉</span><span class="sxs-lookup"><span data-stu-id="02cd1-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="02cd1-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="02cd1-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

