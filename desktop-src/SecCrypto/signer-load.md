---
description: 從指定的 .pfx 檔案載入簽署憑證。
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: 簽署者. Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990069"
---
# <a name="signerload-method"></a><span data-ttu-id="f3a15-103">簽署者. Load 方法</span><span class="sxs-lookup"><span data-stu-id="f3a15-103">Signer.Load method</span></span>

<span data-ttu-id="f3a15-104">\[**Load** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f3a15-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3a15-105">相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="f3a15-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f3a15-106">**Load** 方法會從指定的 .pfx 檔案載入簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="f3a15-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a15-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3a15-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f3a15-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3a15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a15-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="f3a15-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a15-110">包含簽署憑證的 .pfx 檔案名。</span><span class="sxs-lookup"><span data-stu-id="f3a15-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f3a15-111">*密碼* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f3a15-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a15-112">字串，包含用來開啟檔案的純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="f3a15-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="f3a15-113">密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="f3a15-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="f3a15-114">預設值為空字串 ("")。</span><span class="sxs-lookup"><span data-stu-id="f3a15-114">The default value is an empty string ("").</span></span> <span data-ttu-id="f3a15-115">如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a15-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a15-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3a15-116">Return value</span></span>

<span data-ttu-id="f3a15-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3a15-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a15-118">備註</span><span class="sxs-lookup"><span data-stu-id="f3a15-118">Remarks</span></span>

<span data-ttu-id="f3a15-119">這個方法會載入 .pfx 檔案中有相關私密金鑰的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="f3a15-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="f3a15-120">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="f3a15-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a15-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3a15-121">Requirements</span></span>



| <span data-ttu-id="f3a15-122">需求</span><span class="sxs-lookup"><span data-stu-id="f3a15-122">Requirement</span></span> | <span data-ttu-id="f3a15-123">值</span><span class="sxs-lookup"><span data-stu-id="f3a15-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a15-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f3a15-124">Redistributable</span></span><br/> | <span data-ttu-id="f3a15-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f3a15-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f3a15-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a15-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="f3a15-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a15-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a15-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3a15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a15-129">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="f3a15-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
