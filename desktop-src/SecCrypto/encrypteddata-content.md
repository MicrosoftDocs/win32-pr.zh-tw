---
description: 設定或抓取要加密或解密的內容。
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: A 內容屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982285"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="1b276-103">A 內容屬性</span><span class="sxs-lookup"><span data-stu-id="1b276-103">EncryptedData.Content property</span></span>

<span data-ttu-id="1b276-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1b276-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1b276-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。</span><span class="sxs-lookup"><span data-stu-id="1b276-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="1b276-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="1b276-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1b276-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="1b276-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1b276-108">**Content** 屬性會設定或抓取要加密或解密的內容。</span><span class="sxs-lookup"><span data-stu-id="1b276-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="1b276-109">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="1b276-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b276-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b276-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="1b276-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="1b276-111">Property value</span></span>

<span data-ttu-id="1b276-112">要加密或解密的內容。</span><span class="sxs-lookup"><span data-stu-id="1b276-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b276-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b276-113">Requirements</span></span>



| <span data-ttu-id="1b276-114">需求</span><span class="sxs-lookup"><span data-stu-id="1b276-114">Requirement</span></span> | <span data-ttu-id="1b276-115">值</span><span class="sxs-lookup"><span data-stu-id="1b276-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b276-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1b276-116">End of client support</span></span><br/> | <span data-ttu-id="1b276-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b276-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1b276-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1b276-118">End of server support</span></span><br/> | <span data-ttu-id="1b276-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b276-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1b276-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1b276-120">Redistributable</span></span><br/>       | <span data-ttu-id="1b276-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b276-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b276-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1b276-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1b276-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b276-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b276-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b276-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b276-125">**A**</span><span class="sxs-lookup"><span data-stu-id="1b276-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
