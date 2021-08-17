---
title: WinRM 腳本 API
description: Windows遠端系統管理腳本物件會實作為 WS-Management 通訊協定之上的一層。
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742756"
---
# <a name="winrm-scripting-api"></a>WinRM 腳本 API

Windows遠端系統管理腳本物件會實作為[WS-Management 通訊協定](ws-management-protocol.md)之上的一層。 腳本物件可讓您取得資料或管理本機和遠端電腦上的 [*資源*](windows-remote-management-glossary.md) 。

## <a name="ws-management-objects"></a>WS-Management 物件

每個腳本物件都有對應的 c + + 介面。 如需詳細資訊，請參閱[WinRM c + + API](winrm-c---api.md)和[腳本（Windows 遠端管理](scripting-in-windows-remote-management.md)）。

以下是由 WinRM 腳本 API 提供的物件。

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

定義用於遠端連線的使用者名稱和密碼。 呼叫 [**CreateConnectionOptions**](wsman-createconnectionoptions.md) 方法時，會傳遞使用者名稱和密碼。 如需詳細資訊，請參閱 [從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)。 對應的 c + + 介面為 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)。

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**枚舉 數**](enumerator.md)
</dt> <dd>

代表列舉資源時傳回的結果集合。 如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。 對應的 c + + 介面為 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)。

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

提供資源的路徑。 您可以使用 [**ResourceLocator**](resourcelocator.md)物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) ，例如 [**session、Get**](session-get.md)、 [**session、Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。 對應的 c + + 介面為 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)。

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**會話**](session.md)
</dt> <dd>

定義會話可用的網路作業和屬性，例如 [**session. Get**](session-get.md)、 [**session. 列舉**](session-enumerate.md)、 [**session。 Invoke**](session-invoke.md)。 如需詳細資訊，請參閱 [從本機電腦取得資料](obtaining-data-from-the-local-computer.md)。 對應的 c + + 介面為 [**iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)。

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

提供用來建立新會話或管理已建立會話的方法和屬性。 如需詳細資訊，請參閱[使用 Windows 遠端管理](using-windows-remote-management.md)。 對應的 c + + 介面為 [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) 和 [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows遠端系統管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 




