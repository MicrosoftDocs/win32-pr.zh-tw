---
description: 不支援 RKeyPFXInstall 函數。
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: 'RKeyPFXInstall 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943441"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="dfa78-103">RKeyPFXInstall 函式</span><span class="sxs-lookup"><span data-stu-id="dfa78-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="dfa78-104">不支援 **RKeyPFXInstall** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfa78-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="dfa78-105">**Windows Server 2003：\*\*\*\*RKeyPFXInstall** 函式會在遠端電腦上安裝憑證。</span><span class="sxs-lookup"><span data-stu-id="dfa78-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="dfa78-106">請注意，此行為已隨著 Windows Server 2003 Service Pack 1 (SP1) 而變更。</span><span class="sxs-lookup"><span data-stu-id="dfa78-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa78-107">語法</span><span class="sxs-lookup"><span data-stu-id="dfa78-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dfa78-108">參數</span><span class="sxs-lookup"><span data-stu-id="dfa78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa78-109">*hKeySvcCli* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dfa78-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa78-110">[**RKeyOpenKeyService**](rkeyopenkeyservice.md)先前開啟的 [**KEYSVCC \_ 句**](keysvcc-handle.md)柄控制碼。</span><span class="sxs-lookup"><span data-stu-id="dfa78-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="dfa78-111">控制碼代表將接收憑證的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="dfa78-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="dfa78-112">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dfa78-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa78-113">*pPFX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dfa78-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa78-114">[**KEYSVC \_ BLOB**](keysvc-blob.md)結構的指標，代表要安裝的憑證。</span><span class="sxs-lookup"><span data-stu-id="dfa78-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="dfa78-115">BLOB 採用 [*PKCS \# 12*](../secgloss/p-gly.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="dfa78-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="dfa78-116">*pPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dfa78-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa78-117">[**KEYSVC \_ UNICODE \_ 字串**](keysvc-unicode-string.md)結構的指標，表示 BLOB 的密碼。</span><span class="sxs-lookup"><span data-stu-id="dfa78-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="dfa78-118">當您使用完密碼之後，請呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式來清除記憶體中的密碼。</span><span class="sxs-lookup"><span data-stu-id="dfa78-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="dfa78-119">如需保護密碼的詳細資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="dfa78-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa78-120">*ulFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dfa78-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa78-121">指定憑證安裝選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="dfa78-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="dfa78-122">這個參數可以是零或下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="dfa78-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="dfa78-123">值</span><span class="sxs-lookup"><span data-stu-id="dfa78-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="dfa78-124">意義</span><span class="sxs-lookup"><span data-stu-id="dfa78-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="dfa78-125"><dt>**CRYPT \_可匯出**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfa78-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="dfa78-126">匯入的金鑰會標記為可匯出。</span><span class="sxs-lookup"><span data-stu-id="dfa78-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="dfa78-127"><dt>**CRYPT \_電腦 \_ 金鑰集**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfa78-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="dfa78-128">私密金鑰會儲存在遠端電腦上，而不是在目前的使用者底下。</span><span class="sxs-lookup"><span data-stu-id="dfa78-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa78-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfa78-129">Return value</span></span>

<span data-ttu-id="dfa78-130">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="dfa78-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="dfa78-131">如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="dfa78-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa78-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfa78-132">Requirements</span></span>



| <span data-ttu-id="dfa78-133">需求</span><span class="sxs-lookup"><span data-stu-id="dfa78-133">Requirement</span></span> | <span data-ttu-id="dfa78-134">值</span><span class="sxs-lookup"><span data-stu-id="dfa78-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa78-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfa78-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa78-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="dfa78-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="dfa78-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfa78-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa78-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfa78-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfa78-139">標頭</span><span class="sxs-lookup"><span data-stu-id="dfa78-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa78-140"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa78-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa78-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfa78-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa78-142">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="dfa78-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="dfa78-143">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="dfa78-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
