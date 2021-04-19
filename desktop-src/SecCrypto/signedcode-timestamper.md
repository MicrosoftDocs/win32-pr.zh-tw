---
description: TimeStamper 屬性會抓取已簽署之可執行檔的時間戳記程式。
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: SignedCode. TimeStamper 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978492"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="abf31-103">SignedCode. TimeStamper 屬性</span><span class="sxs-lookup"><span data-stu-id="abf31-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="abf31-104">\[**TimeStamper** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="abf31-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="abf31-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="abf31-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="abf31-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="abf31-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="abf31-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="abf31-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="abf31-108">**TimeStamper** 屬性會抓取已簽署之可執行檔的時間戳記程式。</span><span class="sxs-lookup"><span data-stu-id="abf31-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf31-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="abf31-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="abf31-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="abf31-110">Property value</span></span>

<span data-ttu-id="abf31-111">[**簽署者**](signer.md)物件，可讓您存取已簽署的可執行檔的時間戳記程式。</span><span class="sxs-lookup"><span data-stu-id="abf31-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="abf31-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="abf31-112">Requirements</span></span>



| <span data-ttu-id="abf31-113">需求</span><span class="sxs-lookup"><span data-stu-id="abf31-113">Requirement</span></span> | <span data-ttu-id="abf31-114">值</span><span class="sxs-lookup"><span data-stu-id="abf31-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abf31-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="abf31-115">Redistributable</span></span><br/> | <span data-ttu-id="abf31-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="abf31-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="abf31-117">DLL</span><span class="sxs-lookup"><span data-stu-id="abf31-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="abf31-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abf31-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf31-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abf31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf31-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="abf31-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
