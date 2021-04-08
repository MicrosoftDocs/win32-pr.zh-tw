---
description: 提供安全性內容的安全通道特定資訊。
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: 查詢 Schannel 內容的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112168"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a><span data-ttu-id="21849-103">查詢 Schannel 內容的屬性</span><span class="sxs-lookup"><span data-stu-id="21849-103">Querying the Attributes of an Schannel Context</span></span>

<span data-ttu-id="21849-104">[**QueryCoNtextAttributes (schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw)函數提供 [*安全性內容的安全*](../secgloss/s-gly.md)通道特定資訊。</span><span class="sxs-lookup"><span data-stu-id="21849-104">The [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) function provides Schannel-specific information about a [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="21849-105">大部分的資訊最初是在使用用戶端 [**InitializeSecurityCoNtext (schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) 或伺服器 [**AcceptSecurityCoNtext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式建立內容時所指定。</span><span class="sxs-lookup"><span data-stu-id="21849-105">Most of the information is originally specified when the context is created by using the client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) or server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="21849-106">取得用來建立內容之認證的控制碼時，會指定一些資訊。</span><span class="sxs-lookup"><span data-stu-id="21849-106">Some information is specified when obtaining a handle to the credential used to create the context.</span></span> <span data-ttu-id="21849-107">如需詳細資訊，請參閱 [取得 Schannel 認證](obtaining-schannel-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="21849-107">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
