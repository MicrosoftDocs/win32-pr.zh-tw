---
description: QueryCoNtextAttributes (Digest) 函數會提供有關安全性內容目前設定的資訊。
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: 查詢摘要資訊安全內容屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944140"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="378e2-103">查詢摘要資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="378e2-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="378e2-104">[**QueryCoNtextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)函數會提供有關 [*安全性內容*](../secgloss/s-gly.md)目前設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="378e2-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="378e2-105">Microsoft Digest 支援查詢下列安全性內容屬性。</span><span class="sxs-lookup"><span data-stu-id="378e2-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="378e2-106">屬性</span><span class="sxs-lookup"><span data-stu-id="378e2-106">Attribute</span></span>                   | <span data-ttu-id="378e2-107">描述</span><span class="sxs-lookup"><span data-stu-id="378e2-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378e2-108">SECPKG \_ ATTR 索引 \_ 鍵 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="378e2-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="378e2-109">使用中簽署和加密演算法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="378e2-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="378e2-110">SECPKG \_ ATTR \_ 套件 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="378e2-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="378e2-111">關於 Microsoft Digest 的一般資訊，例如 [*安全性套件*](../secgloss/s-gly.md)所允許的權杖大小上限。</span><span class="sxs-lookup"><span data-stu-id="378e2-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="378e2-112">SECPKG \_ ATTR \_ 大小</span><span class="sxs-lookup"><span data-stu-id="378e2-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="378e2-113">訊息相關資料（例如簽章）所允許的大小上限。</span><span class="sxs-lookup"><span data-stu-id="378e2-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
