---
description: 若要簽署檔案並為其建立目錄，您必須先擁有簽署檔案、憑證和公開金鑰的程式。
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: 建立已簽署的檔案和目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193088"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="46ef1-103">建立已簽署的檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="46ef1-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="46ef1-104">若要簽署檔案並為其建立目錄，您必須先擁有簽署檔案、憑證和公開金鑰的程式。</span><span class="sxs-lookup"><span data-stu-id="46ef1-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="46ef1-105">**簽署檔案和建立目錄**</span><span class="sxs-lookup"><span data-stu-id="46ef1-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="46ef1-106">使用 [Pktextract.exe](pktextract-exe.md) 從憑證檔案中解壓縮 [*公開金鑰 token*](p-sbscs-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="46ef1-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="46ef1-107">憑證檔案必須存在於與公用程式相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="46ef1-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="46ef1-108">使用公開金鑰 token 值，在資訊清單檔中更新 **assemblyIdentity** 元素的 **publicKeyToken** 屬性。</span><span class="sxs-lookup"><span data-stu-id="46ef1-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="46ef1-109">使用 [MT.exe](mt-exe.md) 來產生組件資訊清單中包含的檔案雜湊，以及建立目錄描述檔案 ( 的 cdf) 。</span><span class="sxs-lookup"><span data-stu-id="46ef1-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="46ef1-110">使用 Makecat.exe 搭配產生的 cdf 來建立元件的安全性目錄。</span><span class="sxs-lookup"><span data-stu-id="46ef1-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="46ef1-111">此工具組含在 CryptoAPI 中。</span><span class="sxs-lookup"><span data-stu-id="46ef1-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="46ef1-112">使用 [SignTool](/windows/desktop/SecCrypto/signtool) 公用程式來簽署使用步驟1中所使用之憑證所產生的目錄。</span><span class="sxs-lookup"><span data-stu-id="46ef1-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="46ef1-113">建立目錄之後，就可以刪除步驟3和4中的 cdf。</span><span class="sxs-lookup"><span data-stu-id="46ef1-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="46ef1-114">另請參閱 [元件簽署範例](assembly-signing-example.md)。</span><span class="sxs-lookup"><span data-stu-id="46ef1-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
