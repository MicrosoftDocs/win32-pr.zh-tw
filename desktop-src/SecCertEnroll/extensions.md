---
description: X.509 第3版憑證格式可識別多個可新增至憑證的延伸模組。
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: 憑證註冊 API) 的延伸模組 (
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978265"
---
# <a name="extensions-certificate-enrollment-api"></a><span data-ttu-id="7a07e-103">憑證註冊 API) 的延伸模組 (</span><span class="sxs-lookup"><span data-stu-id="7a07e-103">Extensions (Certificate Enrollment API)</span></span>

<span data-ttu-id="7a07e-104">X.509 第3版憑證格式可識別多個可新增至憑證的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7a07e-104">The X.509 version 3 certificate format identifies multiple extensions that can be added to a certificate.</span></span> <span data-ttu-id="7a07e-105">延伸模組提供有關金鑰使用方式、憑證原則和條件約束、替代名稱表單等的增強資訊。</span><span class="sxs-lookup"><span data-stu-id="7a07e-105">The extensions provide enhanced information about key usage, certificate policies and constraints, alternative name forms, and more.</span></span> <span data-ttu-id="7a07e-106">您可以使用 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面來定義延伸模組值。</span><span class="sxs-lookup"><span data-stu-id="7a07e-106">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an extension value.</span></span> <span data-ttu-id="7a07e-107">您可以使用衍生自 **IX509Extension** 的預先定義介面來建立許多常見的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7a07e-107">Many of the common extensions can be created by using predefined interfaces derived from **IX509Extension**.</span></span> <span data-ttu-id="7a07e-108">擴充功能的集合會在要求屬性中包含集合，藉此新增至憑證要求。</span><span class="sxs-lookup"><span data-stu-id="7a07e-108">A collection of extensions is added to a certificate request by including the collection in the request attributes.</span></span> <span data-ttu-id="7a07e-109">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="7a07e-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7a07e-110">支援的延伸模組</span><span class="sxs-lookup"><span data-stu-id="7a07e-110">Supported Extensions</span></span>](supported-extensions.md)
-   [<span data-ttu-id="7a07e-111">PKCS \# 10 擴充功能</span><span class="sxs-lookup"><span data-stu-id="7a07e-111">PKCS \#10 Extensions</span></span>](pkcs--10-extensions.md)
-   [<span data-ttu-id="7a07e-112">CMC 延伸模組</span><span class="sxs-lookup"><span data-stu-id="7a07e-112">CMC Extensions</span></span>](cmc-extensions.md)

 

 



