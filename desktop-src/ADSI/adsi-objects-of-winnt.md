---
title: WinNT 的 ADSI 物件
description: ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI、ADSI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f3d2cb845e7fa6c754198abbb9a274987f69a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467385"
---
# <a name="adsi-objects-of-winnt"></a>WinNT 的 ADSI 物件

ADSI WinNT 提供者會執行下列 COM 物件，以支援各種 ADSI 介面的功能和服務。




| ADSI 物件 | Description | 支援的介面 | 
|-------------|-------------|----------------------|
| <strong>類別</strong> | 表示類別定義的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>得到 iadsclass</strong></a></dt></dl> | 
| <strong>電腦</strong> | 代表電腦的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>網域</strong> | 透過網路表示網域的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileService</strong> | 代表檔案服務的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileShare</strong> | 代表檔案共用的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWFileService</strong> | 代表檔案服務的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>FPNWFileShare</strong> | 代表檔案共用的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResource</strong> | 代表資源的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResourcesCollection</strong> | 代表資源集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>FPNWSession</strong> | 表示會話的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWSessionsCollection</strong> | 表示會話集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>群組</strong> | 代表群組的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl><blockquote>[!Note]<br />GetInfo 不能用於包含在 WinNT 範圍中 W w n 安全性主體之成員的群組。</blockquote><br /> | 
| <strong>GroupCollection</strong> | 表示群組集合的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>LocalGroup</strong> | 表示本機群組的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>LocalgroupCollection</strong> | 表示本機群組集合的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Namespace</strong> | 表示 WinNT 命名空間的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt></dl> | 
| <strong>PrintJob</strong> | 表示列印工作的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>PrintJobsCollection</strong> | 表示列印工作集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>PrintQueue</strong> | 表示列印佇列的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>屬性</strong> | 表示屬性定義的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt></dl> | 
| <strong>Resource</strong> | 代表資源的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>ResourcesCollection</strong> | 代表資源集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>結構描述</strong> | 表示架構容器的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>服務</strong> | 代表服務的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>工作階段</strong> | 表示會話的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>SessionsCollection</strong> | 表示會話集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>語法</strong> | 表示屬性語法的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt></dl> | 
| <strong>使用者</strong> | 表示使用者帳戶的 ADSI 物件。 | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>UserGroupCollection</strong> | 表示使用者群組集合的 ADSI 物件。 | <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a> | 




 

 

 





