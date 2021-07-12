---
description: Cert2spc.exe
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2spc.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581976"
---
# <a name="cert2spc"></a><span data-ttu-id="68375-103">Cert2spc.exe</span><span class="sxs-lookup"><span data-stu-id="68375-103">Cert2SPC</span></span>

<span data-ttu-id="68375-104">cert2spc.exe 工具會使用現有的 [*x.509*](../secgloss/x-gly.md) [*憑證*](../secgloss/c-gly.md)， [*Publisher 憑證*](../secgloss/s-gly.md) (SPC) 建立測試軟體。</span><span class="sxs-lookup"><span data-stu-id="68375-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="68375-105">Cert2spc.exe 可將多個 x.509 憑證包裝到 [*PKCS \# 7*](../secgloss/p-gly.md) 的已簽署資料物件中。</span><span class="sxs-lookup"><span data-stu-id="68375-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="68375-106">此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="68375-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="68375-107">cert2spc.exe 可做為 Windows SDK 的一部分，可供您下載 <https://go.microsoft.com/fwlink/p/?linkid=84091> 。</span><span class="sxs-lookup"><span data-stu-id="68375-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="68375-108">此工具僅供測試之用。</span><span class="sxs-lookup"><span data-stu-id="68375-108">This tool is for test purposes only.</span></span> <span data-ttu-id="68375-109">從 [*憑證授權單位*](../secgloss/c-gly.md)單位取得有效的 SPC。</span><span class="sxs-lookup"><span data-stu-id="68375-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="68375-110">**Cert2spc.exe** *Cert1 .cer Cert2 .cer* .。。</span><span class="sxs-lookup"><span data-stu-id="68375-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="68375-111">*輸出 spc*</span><span class="sxs-lookup"><span data-stu-id="68375-111">*Output.spc*</span></span>

 



| <span data-ttu-id="68375-112">參數</span><span class="sxs-lookup"><span data-stu-id="68375-112">Parameters</span></span>              | <span data-ttu-id="68375-113">描述</span><span class="sxs-lookup"><span data-stu-id="68375-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68375-114">*Cert1 .Cer Cert2 .cer* .。。</span><span class="sxs-lookup"><span data-stu-id="68375-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="68375-115">要包含在 SPC 中的 x.509 憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="68375-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="68375-116">每個憑證名稱的結尾都是 .cer 副檔名。</span><span class="sxs-lookup"><span data-stu-id="68375-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="68375-117">*輸出 spc*</span><span class="sxs-lookup"><span data-stu-id="68375-117">*Output.spc*</span></span>            | <span data-ttu-id="68375-118">PKCS \# 7 物件的名稱，其中包含要建立的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="68375-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="68375-119">輸出檔名稱以 .spc 副檔名結尾。</span><span class="sxs-lookup"><span data-stu-id="68375-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
