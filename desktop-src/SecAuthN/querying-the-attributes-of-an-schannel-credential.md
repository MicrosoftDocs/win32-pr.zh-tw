---
description: 提供有關認證的 Schannel 特定資訊。
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: 查詢 Schannel 認證的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192625"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="bba9e-103">查詢 Schannel 認證的屬性</span><span class="sxs-lookup"><span data-stu-id="bba9e-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="bba9e-104">[**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa)函式會提供有關認證的 Schannel 特定資訊。</span><span class="sxs-lookup"><span data-stu-id="bba9e-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="bba9e-105">這項資訊最初是在建立認證時指定。</span><span class="sxs-lookup"><span data-stu-id="bba9e-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="bba9e-106">如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="bba9e-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="bba9e-107">此函數所報告的資訊適用于任何 ([*安全性*](../secgloss/s-gly.md) 內容) 使用指定的認證建立的連接。</span><span class="sxs-lookup"><span data-stu-id="bba9e-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
