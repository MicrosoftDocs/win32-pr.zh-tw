---
description: SSPI 的設計可讓您撰寫其他 Ssp 並將其新增至系統。
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: 撰寫和安裝安全性支援提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975137"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="08d03-103">撰寫和安裝安全性支援提供者</span><span class="sxs-lookup"><span data-stu-id="08d03-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="08d03-104">SSPI 的設計可讓您撰寫其他 Ssp 並將其新增至系統。</span><span class="sxs-lookup"><span data-stu-id="08d03-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="08d03-105">您可以根據與作業系統的整合層級，以相對較簡單或很大的複雜度來開發安全性模型專屬的 [*SSP*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="08d03-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="08d03-106">允許連接到新類型伺服器的用戶端 SSP 可以非常快速地進行開發，而提供本機模擬的完整 SSP 需要更多投入時間。</span><span class="sxs-lookup"><span data-stu-id="08d03-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="08d03-107">您可以藉由更新登錄中的 **REG \_ SZ** 值來安裝 ssp，如下所示：</span><span class="sxs-lookup"><span data-stu-id="08d03-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="08d03-108">**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **>hklm\system\system\currentcontrolset\control\securityproviders\schannel\protocols\tls**  =  *Provider1.dll，Provider2.dll，*.。。    </span><span class="sxs-lookup"><span data-stu-id="08d03-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="08d03-109">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="08d03-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="08d03-110">單一 DLL 可以包含多個 Ssp。</span><span class="sxs-lookup"><span data-stu-id="08d03-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08d03-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="08d03-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d03-112">註冊和安裝安全性套件的限制</span><span class="sxs-lookup"><span data-stu-id="08d03-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
