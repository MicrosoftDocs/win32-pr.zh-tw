---
title: WinRM c + + API
description: Windows 遠端管理介面可以用來取得資料或管理遠端電腦上的資源。 此 API 主要是供內部使用。 建議您盡可能使用 WinRM 用戶端 Shell API。
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742944"
---
# <a name="winrm-c-api"></a>WinRM c + + API

Windows 遠端管理介面可以用來取得資料或管理遠端電腦上的 [*資源*](windows-remote-management-glossary.md)。 此 API 主要是供內部使用。 建議您盡可能使用 [WinRM 用戶端 SHELL API](client-shell-api.md) 。 介面會緊密對應至 [WinRM 腳本 API](winrm-scripting-api.md)。

直接從 **IDispatch** 繼承的 WinRM 介面具有對應的腳本物件。 如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。

針對多執行緒應用程式，WinRM 不支援存取相同 [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) 物件的個別執行緒。

下列是 WinRM 提供的介面。

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

提供用來建立新會話和管理已建立會話的方法和屬性。 [**WSMan**](wsman.md) 是對應的腳本物件。

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

提供用來建立新 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)的方法和屬性。 這種方法適用于 [**WSMan**](wsman.md) 腳本物件。

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

定義用於遠端連線的使用者名稱和密碼。 [**ConnectionOptions**](connectionoptions.md) 是對應的腳本物件。

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**Iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

定義會話可用的網路作業和屬性。 [**Session**](session.md) 是對應的腳本物件。

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

代表列舉資源時傳回的結果集合。 [**列舉**](enumerator.md) 值是對應的腳本物件。

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

提供資源的路徑。 您可以使用 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) 。 [**ResourceLocator**](resourcelocator.md) 是對應的腳本物件。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows遠端系統管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 




