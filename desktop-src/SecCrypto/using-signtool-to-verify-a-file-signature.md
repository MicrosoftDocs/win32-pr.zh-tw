---
description: 說明如何使用 SignTool 來驗證檔案簽章。
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: 使用 SignTool 來驗證檔案簽章
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954921"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="44514-103">使用 SignTool 來驗證檔案簽章</span><span class="sxs-lookup"><span data-stu-id="44514-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="44514-104">下列命令會驗證名為 *MyControl.exe* 之檔案的簽章：</span><span class="sxs-lookup"><span data-stu-id="44514-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="44514-105">**SignTool 確認** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="44514-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="44514-106">如果上述範例失敗，可能是簽章使用程式碼簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="44514-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="44514-107">[SignTool](signtool.md) 預設為 Windows 驅動程式原則以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="44514-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="44514-108">下列命令會使用預設驗證驗證原則來驗證簽章：</span><span class="sxs-lookup"><span data-stu-id="44514-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="44514-109">**SignTool 確認/pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="44514-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="44514-110">下列命令會驗證可能已在目錄中簽署的系統檔案：</span><span class="sxs-lookup"><span data-stu-id="44514-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="44514-111">**SignTool 確認/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="44514-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="44514-112">下列命令會驗證在名為 *MyCat.cat* 的目錄中簽署的系統檔案：</span><span class="sxs-lookup"><span data-stu-id="44514-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="44514-113">**SignTool 驗證/c** *MyCat.cat* *MyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="44514-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span></span>

<span data-ttu-id="44514-114">針對任何 [SignTool](signtool.md) 驗證，您可以取得憑證的簽署者。</span><span class="sxs-lookup"><span data-stu-id="44514-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="44514-115">下列命令會驗證系統檔案並顯示簽署者憑證：</span><span class="sxs-lookup"><span data-stu-id="44514-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="44514-116">**SignTool 確認/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="44514-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="44514-117">[SignTool](signtool.md) 會傳回命令列文字，指出簽章檢查的結果。</span><span class="sxs-lookup"><span data-stu-id="44514-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="44514-118">此外，SignTool 會傳回零的結束代碼，表示執行成功，一個用於失敗的執行，另二個則表示執行完成但出現警告。</span><span class="sxs-lookup"><span data-stu-id="44514-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="44514-119">如需 [SignTool](signtool.md)的詳細資訊，請參閱 [SignTool](signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="44514-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



