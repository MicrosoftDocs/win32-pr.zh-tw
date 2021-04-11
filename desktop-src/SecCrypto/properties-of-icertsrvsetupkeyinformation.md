---
description: 下列屬性是由 ICertSrvSetupKeyInformation 介面所定義。
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: ICertSrvSetupKeyInformation 的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849459"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="ac0f3-103">ICertSrvSetupKeyInformation 的屬性</span><span class="sxs-lookup"><span data-stu-id="ac0f3-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="ac0f3-104">下列屬性是由 [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="ac0f3-105">屬性</span><span class="sxs-lookup"><span data-stu-id="ac0f3-105">Property</span></span>                                                                           | <span data-ttu-id="ac0f3-106">描述</span><span class="sxs-lookup"><span data-stu-id="ac0f3-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac0f3-107">**容器**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="ac0f3-108">取得或設定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 用來產生、儲存或存取金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="ac0f3-109">**Existing**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="ac0f3-110">取得或設定值，這個值表示私密金鑰是否已存在。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="ac0f3-111">**ExistingCACertificate**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="ac0f3-112">取得或設定已使用 [*可辨別編碼規則*](../secgloss/d-gly.md) (DER) 編碼的二進位值，也就是對應至現有金鑰的 CA 憑證的二進位值。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="ac0f3-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="ac0f3-114">取得或設定雜湊演算法的名稱，此雜湊演算法用來簽署或驗證金鑰的 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="ac0f3-115">**長度**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="ac0f3-116">取得或設定金鑰的強度為 CSP 所支援的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="ac0f3-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="ac0f3-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="ac0f3-118">取得或設定用來產生或儲存私密金鑰的 CSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0f3-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
