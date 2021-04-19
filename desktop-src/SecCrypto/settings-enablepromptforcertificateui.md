---
description: 設定或取得布林值，這個值會指定是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: EnablePromptForCertificateUI 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990673"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="44aab-103">EnablePromptForCertificateUI 屬性</span><span class="sxs-lookup"><span data-stu-id="44aab-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="44aab-104">\[**EnablePromptForCertificateUI** 屬性可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="44aab-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="44aab-105">**EnablePromptForCertificateUI** 屬性會設定或取得布林值，這個值會指定是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="44aab-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="44aab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="44aab-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="44aab-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="44aab-107">Property value</span></span>

<span data-ttu-id="44aab-108">若 **為 true**，則可使用使用者介面提示輸入簽署者或寄件者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="44aab-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="44aab-109">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="44aab-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="44aab-110">設定這個屬性並不會停用從 web 應用程式完成任何私密金鑰使用之前所產生的警告。</span><span class="sxs-lookup"><span data-stu-id="44aab-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44aab-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="44aab-111">Requirements</span></span>



| <span data-ttu-id="44aab-112">需求</span><span class="sxs-lookup"><span data-stu-id="44aab-112">Requirement</span></span> | <span data-ttu-id="44aab-113">值</span><span class="sxs-lookup"><span data-stu-id="44aab-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44aab-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="44aab-114">Redistributable</span></span><br/> | <span data-ttu-id="44aab-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="44aab-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44aab-116">DLL</span><span class="sxs-lookup"><span data-stu-id="44aab-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="44aab-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44aab-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44aab-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44aab-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44aab-119">**設定**</span><span class="sxs-lookup"><span data-stu-id="44aab-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




