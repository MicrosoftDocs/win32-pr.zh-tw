---
title: 伺服器資料物件介面
description: 伺服器資料物件 (SDO) API 會公開下列介面。
ms.assetid: c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0c5105194056e70855c390c40011075c7718a7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383070"
---
# <a name="server-data-objects-interfaces"></a><span data-ttu-id="5e167-103">伺服器資料物件介面</span><span class="sxs-lookup"><span data-stu-id="5e167-103">Server Data Objects Interfaces</span></span>

<span data-ttu-id="5e167-104">伺服器資料物件 (SDO) API 會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="5e167-104">The Server Data Objects (SDO) API exposes the following interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e167-105">介面</span><span class="sxs-lookup"><span data-stu-id="5e167-105">Interface</span></span></th>
<th><span data-ttu-id="5e167-106">目的</span><span class="sxs-lookup"><span data-stu-id="5e167-106">Purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e167-107"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdo"><strong>ISdo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e167-107"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdo"><strong>ISdo</strong></a></span></span></td>
<td><span data-ttu-id="5e167-108">操作 SDO 物件。</span><span class="sxs-lookup"><span data-stu-id="5e167-108">Manipulate an SDO object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e167-109"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection"><strong>ISdoCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e167-109"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection"><strong>ISdoCollection</strong></a></span></span></td>
<td><span data-ttu-id="5e167-110">操作 SDO 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="5e167-110">Manipulate a collection of SDO objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e167-111"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold"><strong>ISdoDictionaryOld</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e167-111"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold"><strong>ISdoDictionaryOld</strong></a></span></span></td>
<td><span data-ttu-id="5e167-112">操作屬性字典。</span><span class="sxs-lookup"><span data-stu-id="5e167-112">Manipulate the attribute dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e167-113"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine"><strong>ISdoMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e167-113"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine"><strong>ISdoMachine</strong></a></span></span></td>
<td><span data-ttu-id="5e167-114">管理 SDO 電腦，並取出 SDO 物件。</span><span class="sxs-lookup"><span data-stu-id="5e167-114">Manage the SDO computer, and retrieve SDO objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5e167-115"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol"><strong>ISdoServiceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5e167-115"><a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol"><strong>ISdoServiceControl</strong></a></span></span></td>
<td><span data-ttu-id="5e167-116">管理透過 SDO 管理的服務，也就是網際網路驗證服務 (IAS) 或遠端存取服務器 (RAS) 。</span><span class="sxs-lookup"><span data-stu-id="5e167-116">Manage the service being administered through SDO, that is, either Internet Authentication Service (IAS) or Remote Access Server (RAS).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5e167-117">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="5e167-117">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

