---
description: 如果您使用適用于 WMI 的腳本 API，您可以設定特定的安全性許可權。
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: 使用 VBScript 執行特殊許可權作業
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115860"
---
# <a name="executing-privileged-operations-using-vbscript"></a>使用 VBScript 執行特殊許可權作業

如果您使用適用于 WMI 的腳本 API，您可以設定特定的安全性許可權。 例如，您可以設定安全性許可權來要求作業系統關機，或是檢查安全性事件記錄檔。 如需詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

當您在電腦上存取 WMI 時，只需要設定許可權。 當您存取遠端主機時，COM RPC 會自動設定許可權。 若要判斷所有必要的許可權，請參閱您要存取的特定 WMI 類別的檔，例如 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)。 如需詳細資訊，請參閱 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

本主題將討論下列各節：

-   [從安全性物件設定許可權 \_](/windows)
-   [將許可權設定為標記的一部分](#setting-a-privilege-as-part-of-a-moniker)
-   [撤銷和重設許可權](#revoking-and-resetting-privileges)
-   [相關主題](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>從安全性物件設定許可權 \_

使用下列程式，在 Visual Basic 中設定安全性許可權。

**若要在 Visual Basic 中設定許可權**

1.  建立 [**wbemscripting.swbemlocator**](swbemlocator.md)類型的物件。
2.  將新的許可權新增至 [**wbemscripting.swbemlocator. Security \_**](swbemlocator-security-.md)物件。

    [**安全性 \_**](swbemlocator-security-.md)物件包含 [**swbemobjectset 搭配使用**](swbemobjectset.md)集合。 集合中的物件是 [**SWbemSecurity**](swbemsecurity.md) 物件。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

3.  登入 WMI 並取出 [**SWbemServices**](swbemservices.md) 物件。

    [**SWbemServices**](swbemservices.md)物件會繼承在上一個步驟中設定的許可權。

您也可以使用 [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) 方法來設定許可權。

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>將許可權設定為標記的一部分

您可以將許可權設定為「標記」的一部分。

下列範例示範如何將 debug 許可權加入至標記。


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>撤銷和重設許可權

下列範例會示範如何設定 **SeDebugPrivilege** 許可權，以及撤銷 **SeRemoteShutdownPrivilege** 許可權。


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**許可權常數**](privilege-constants.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> </dl>

 

 
