---
description: 解密封裝的內容。
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData 解密方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998810"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="baba0-103">EnvelopedData 解密方法</span><span class="sxs-lookup"><span data-stu-id="baba0-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="baba0-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="baba0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="baba0-105">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="baba0-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="baba0-106">**解密** 方法會解密已封裝的內容。</span><span class="sxs-lookup"><span data-stu-id="baba0-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="baba0-107">如果訊息的收件者可以存取與用來波封訊息的其中一個 [*公開金鑰*](../secgloss/p-gly.md)配對的 [*私密金鑰*](../secgloss/p-gly.md)，則會進行解密。</span><span class="sxs-lookup"><span data-stu-id="baba0-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="baba0-108">呼叫 **解密** 方法會重設物件的 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="baba0-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="baba0-109">如果 **解密** 方法成功， [**EnvelopedData**](envelopeddata.md)物件的 [**Content**](envelopeddata-content.md)屬性會設定為純文字訊息。</span><span class="sxs-lookup"><span data-stu-id="baba0-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="baba0-110">語法</span><span class="sxs-lookup"><span data-stu-id="baba0-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="baba0-111">參數</span><span class="sxs-lookup"><span data-stu-id="baba0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baba0-112">*EnvelopedMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="baba0-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baba0-113">字串，包含要解密的封包資料。</span><span class="sxs-lookup"><span data-stu-id="baba0-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baba0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="baba0-114">Return value</span></span>

<span data-ttu-id="baba0-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="baba0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baba0-116">備註</span><span class="sxs-lookup"><span data-stu-id="baba0-116">Remarks</span></span>

<span data-ttu-id="baba0-117">解密的資料會變成 [**EnvelopedData**](envelopeddata.md)物件的 [**Content**](envelopeddata-content.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="baba0-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="baba0-118">如果這個方法的使用者無法存取符合其中一個用來波封訊息之公開金鑰的私密金鑰，該方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="baba0-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="baba0-119">如果相關聯的私密金鑰的憑證不在 [本機電腦] 或 [目前使用者] 存放區中，則此方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="baba0-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="baba0-120">從 web 腳本呼叫這個方法時，腳本必須使用您的 [*私密金鑰*](../secgloss/p-gly.md) 來解密資料。</span><span class="sxs-lookup"><span data-stu-id="baba0-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="baba0-121">允許不受信任的網站使用您的私密金鑰會有安全性風險。</span><span class="sxs-lookup"><span data-stu-id="baba0-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="baba0-122">當第一次呼叫此方法時，會詢問網站是否可以使用您的私密金鑰的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="baba0-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="baba0-123">如果您允許腳本使用您的私密金鑰，然後選取 [不要再詢問我]，就不會再出現任何使用您私密金鑰的腳本來解密該網域內的資料。</span><span class="sxs-lookup"><span data-stu-id="baba0-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="baba0-124">不過，嘗試使用私密金鑰來解密資料的網域以外的腳本仍會導致這個對話方塊出現。</span><span class="sxs-lookup"><span data-stu-id="baba0-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="baba0-125">如果您不允許腳本使用您的私密金鑰，然後選取 [不要再詢問我]，則該網域內的腳本將會自動拒絕使用您私密金鑰來解密資料的能力。</span><span class="sxs-lookup"><span data-stu-id="baba0-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="baba0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="baba0-126">Requirements</span></span>



| <span data-ttu-id="baba0-127">需求</span><span class="sxs-lookup"><span data-stu-id="baba0-127">Requirement</span></span> | <span data-ttu-id="baba0-128">值</span><span class="sxs-lookup"><span data-stu-id="baba0-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baba0-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="baba0-129">End of client support</span></span><br/> | <span data-ttu-id="baba0-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baba0-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="baba0-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="baba0-131">End of server support</span></span><br/> | <span data-ttu-id="baba0-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baba0-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="baba0-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="baba0-133">Redistributable</span></span><br/>       | <span data-ttu-id="baba0-134">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="baba0-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="baba0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="baba0-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="baba0-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baba0-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baba0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baba0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baba0-138">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="baba0-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="baba0-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="baba0-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
