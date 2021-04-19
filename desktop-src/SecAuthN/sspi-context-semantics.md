---
description: 安全性內容是在通訊會話期間有效的一組安全性屬性和規則。
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: SSPI 內容語義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994446"
---
# <a name="sspi-context-semantics"></a><span data-ttu-id="91514-103">SSPI 內容語義</span><span class="sxs-lookup"><span data-stu-id="91514-103">SSPI Context Semantics</span></span>

<span data-ttu-id="91514-104">[*安全性內容*](../secgloss/s-gly.md)是在通訊會話期間有效的一組安全性屬性和規則。</span><span class="sxs-lookup"><span data-stu-id="91514-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="91514-105">這包括主體身分識別的資訊，以及所使用金鑰、密碼和演算法的資訊。</span><span class="sxs-lookup"><span data-stu-id="91514-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="91514-106">針對 [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) ，安全性內容是一種不透明的結構，此結構是透過包含 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式和 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式的結算所建立。</span><span class="sxs-lookup"><span data-stu-id="91514-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="91514-107">如需內容屬性的詳細資訊，請參閱 [內容需求](context-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91514-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="91514-108">SSPI 模型支援三種類型的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="91514-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91514-109">類型</span><span class="sxs-lookup"><span data-stu-id="91514-109">Type</span></span></th>
<th><span data-ttu-id="91514-110">描述</span><span class="sxs-lookup"><span data-stu-id="91514-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91514-111"><a href="connection-oriented-contexts.md">[連接]</a></span><span class="sxs-lookup"><span data-stu-id="91514-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="91514-112">連接導向的 <a href="/windows/desktop/SecGloss/c-gly"><em>內容</em></a> 是最常見的安全性內容，而且是最簡單的使用方式。</span><span class="sxs-lookup"><span data-stu-id="91514-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="91514-113">呼叫端會負責整體訊息格式和訊息中資料的位置。</span><span class="sxs-lookup"><span data-stu-id="91514-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="91514-114">呼叫端也負責訊息內安全性相關欄位的位置，例如簽章資料的位置。</span><span class="sxs-lookup"><span data-stu-id="91514-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91514-115"><a href="datagram-contexts.md">資料包</a></span><span class="sxs-lookup"><span data-stu-id="91514-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="91514-116"><a href="/windows/desktop/SecGloss/d-gly"><em>資料包</em></a>導向內容具有 DCE 樣式資料包通訊的額外支援。</span><span class="sxs-lookup"><span data-stu-id="91514-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="91514-117">它也可以一般用於資料包導向的傳輸應用程式。</span><span class="sxs-lookup"><span data-stu-id="91514-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="91514-118"><a href="microsoft-kerberos.md">Microsoft Kerberos</a>套件不支援使用者到使用者模式中的資料包內容。</span><span class="sxs-lookup"><span data-stu-id="91514-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91514-119"><a href="stream-contexts.md">串流</a></span><span class="sxs-lookup"><span data-stu-id="91514-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="91514-120">資料流程導向內容負責安全性封裝內的封鎖和訊息格式化。</span><span class="sxs-lookup"><span data-stu-id="91514-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="91514-121">呼叫端不感興趣格式化，而是資料的原始資料流程。</span><span class="sxs-lookup"><span data-stu-id="91514-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="91514-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="91514-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91514-123">內容需求</span><span class="sxs-lookup"><span data-stu-id="91514-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="91514-124">連線導向的內容</span><span class="sxs-lookup"><span data-stu-id="91514-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="91514-125">資料包內容</span><span class="sxs-lookup"><span data-stu-id="91514-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="91514-126">資料流程內容</span><span class="sxs-lookup"><span data-stu-id="91514-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
