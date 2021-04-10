---
description: 用戶端和伺服器憑證都必須儲存在應用程式進程可存取的憑證存放區中。
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: 憑證存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026501"
---
# <a name="certificate-stores"></a><span data-ttu-id="3fff8-103">憑證存放區</span><span class="sxs-lookup"><span data-stu-id="3fff8-103">Certificate Stores</span></span>

<span data-ttu-id="3fff8-104">[*用戶端*](/windows/desktop/SecGloss/c-gly)和 [*伺服器憑證*](/windows/desktop/SecGloss/s-gly)都必須儲存在應用程式進程可存取的 [*憑證存放區*](/windows/desktop/SecGloss/c-gly)中。</span><span class="sxs-lookup"><span data-stu-id="3fff8-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="3fff8-105">一般而言，這是「我的存放區」，也稱為「個人」存放區。</span><span class="sxs-lookup"><span data-stu-id="3fff8-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="3fff8-106">像 Internet Explorer 的用戶端應用程式通常會使用目前使用者的「我的存放區」，而伺服器（例如 Internet Information Services (IIS) 使用本機電腦的「系統」存放區。</span><span class="sxs-lookup"><span data-stu-id="3fff8-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="3fff8-107">當 Schannel 或應用程式建立要傳送至遠端電腦的憑證鏈時，會使用根存放區和 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位 (CA) 存放區。</span><span class="sxs-lookup"><span data-stu-id="3fff8-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="3fff8-108">這些存放區用來驗證已接收的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="3fff8-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="3fff8-109">如需詳細資訊，請參閱 [使用 Schannel 執行驗證](performing-authentication-using-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="3fff8-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
