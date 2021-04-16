---
description: 下列命令會將 x.509 憑證（Mycert.cer）包裝到測試 PKCS \# 7 軟體發行者憑證 (SPC) （稱為 mycert.cer）。
ms.assetid: c3287289-d2bf-4d1d-80f0-e7dd41a3cbe3
title: 使用 Cert2spc.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca10b0ab121e283a181c84b056b63ce10ece385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512408"
---
# <a name="using-cert2spc"></a><span data-ttu-id="27fe2-103">使用 Cert2spc.exe</span><span class="sxs-lookup"><span data-stu-id="27fe2-103">Using Cert2SPC</span></span>

<span data-ttu-id="27fe2-104">下列命令會將 [*x.509*](../secgloss/x-gly.md) 憑證（ *mycert.cer*）包裝到測試 PKCS \# 7 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPC) （稱為 *mycert.cer*）。</span><span class="sxs-lookup"><span data-stu-id="27fe2-104">The following command wraps an [*X.509*](../secgloss/x-gly.md) certificate, *MyCert*.cer, into a test PKCS \#7 [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC), called *MyCert*.spc.</span></span> <span data-ttu-id="27fe2-105">所建立的 SPC 僅供測試用途使用。</span><span class="sxs-lookup"><span data-stu-id="27fe2-105">The SPC created is to be used for test purposes only.</span></span> <span data-ttu-id="27fe2-106">用來實際簽署要散發至公用之程式碼的 SPC，必須從 GTE、VeriSign、Inc. 或其他受信任的 [*憑證授權單位*](../secgloss/c-gly.md) 單位（ (CA) 取得。</span><span class="sxs-lookup"><span data-stu-id="27fe2-106">An SPC used to actually sign code to be distributed to the public must be obtained from GTE, VeriSign, Inc., or another trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="27fe2-107">**Cert2spc.exe** *mycert.cer \* \* \* .cer* \*  *mycert.cer \* \* \* .spc*\*</span><span class="sxs-lookup"><span data-stu-id="27fe2-107">**Cert2SPC** *MyCert\*\*\*.cer*\* *MyCert\*\*\*.spc*\*</span></span>

 

 
