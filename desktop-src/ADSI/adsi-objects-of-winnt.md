---
title: WinNT 的 ADSI 物件
description: ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI、ADSI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93332a2b0501c9c7c4140d83ff7358f18ae68adc50f9f9f3b689765d947ef01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180582"
---
# <a name="adsi-objects-of-winnt"></a>WinNT 的 ADSI 物件

ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ADSI 物件</th>
<th>Description</th>
<th>支援的介面</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>類別</strong></td>
<td>表示類別定義的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>得到 iadsclass</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>電腦</strong></td>
<td>代表電腦的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>網域</strong></td>
<td>透過網路表示網域的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>代表檔案服務的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>代表檔案共用的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWFileService</strong></td>
<td>代表檔案服務的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWFileShare</strong></td>
<td>代表檔案共用的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWResource</strong></td>
<td>代表資源的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWResourcesCollection</strong></td>
<td>代表資源集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>FPNWSession</strong></td>
<td>表示會話的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWSessionsCollection</strong></td>
<td>表示會話集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>群組</strong></td>
<td>代表群組的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
GetInfo 不能用於包含在 WinNT 範圍中 W w n 安全性主體之成員的群組。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>表示群組集合的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>LocalGroup</strong></td>
<td>表示本機群組的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>LocalgroupCollection</strong></td>
<td>表示本機群組集合的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Namespace</strong></td>
<td>表示 WinNT 命名空間的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>PrintJob</strong></td>
<td>表示列印工作的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>PrintJobsCollection</strong></td>
<td>表示列印工作集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>表示列印佇列的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>屬性</strong></td>
<td>表示屬性定義的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Resource</strong></td>
<td>代表資源的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>ResourcesCollection</strong></td>
<td>代表資源集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>結構描述</strong></td>
<td>表示架構容器的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>服務</strong></td>
<td>代表服務的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>工作階段</strong></td>
<td>表示會話的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>SessionsCollection</strong></td>
<td>表示會話集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>語法</strong></td>
<td>表示屬性語法的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>使用者</strong></td>
<td>表示使用者帳戶的 ADSI 物件。</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>UserGroupCollection</strong></td>
<td>表示使用者群組集合的 ADSI 物件。</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





