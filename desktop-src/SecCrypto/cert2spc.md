---
description: Cert2spc.exe
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2spc.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106989131"
---
# <a name="cert2spc"></a><span data-ttu-id="a6a5e-103">Cert2spc.exe</span><span class="sxs-lookup"><span data-stu-id="a6a5e-103">Cert2SPC</span></span>

<span data-ttu-id="a6a5e-104">Cert2spc.exe 工具會使用現有的 [*x.509*](../secgloss/x-gly.md) [*憑證*](../secgloss/c-gly.md)來建立 (SPC) 的測試 [*軟體發行者憑證*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="a6a5e-105">Cert2spc.exe 可將多個 x.509 憑證包裝到 [*PKCS \# 7*](../secgloss/p-gly.md) 的已簽署資料物件中。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="a6a5e-106">此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="a6a5e-107">Cert2spc.exe 可做為 Windows SDK 的一部分，可供您下載 <https://go.microsoft.com/fwlink/p/?linkid=84091> 。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="a6a5e-108">此工具僅供測試之用。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-108">This tool is for test purposes only.</span></span> <span data-ttu-id="a6a5e-109">從 [*憑證授權單位*](../secgloss/c-gly.md)單位取得有效的 SPC。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="a6a5e-110">**Cert2spc.exe** *Cert1 .cer Cert2 .cer* .。。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="a6a5e-111">*輸出 spc*</span><span class="sxs-lookup"><span data-stu-id="a6a5e-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a5e-112">*Cert1 .Cer Cert2 .cer* .。。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="a6a5e-113">要包含在 SPC 中的 x.509 憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="a6a5e-114">每個憑證名稱的結尾都是 .cer 副檔名。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="a6a5e-115">*輸出 spc*</span><span class="sxs-lookup"><span data-stu-id="a6a5e-115">*Output.spc*</span></span>            | <span data-ttu-id="a6a5e-116">PKCS \# 7 物件的名稱，其中包含要建立的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="a6a5e-117">輸出檔名稱以 .spc 副檔名結尾。</span><span class="sxs-lookup"><span data-stu-id="a6a5e-117">The output file name ends with the .spc extension.</span></span> |



 

 

 
