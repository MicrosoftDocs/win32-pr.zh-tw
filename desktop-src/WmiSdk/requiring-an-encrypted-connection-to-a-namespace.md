---
description: 您可以要求用戶端腳本和應用程式建立加密連接以進行驗證，方法是將 RequiresEncryption 限定詞新增至建立命名空間的受控物件格式 (MOF) mof 檔案。
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: 需要命名空間的加密連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996982"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>需要命名空間的加密連接

您可以要求用戶端腳本和應用程式建立加密連接以進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的受控物件格式 (mof) mof 檔案。


對 WMI 命名空間進行加密的連線，會在腳本) 中指定 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權** (或 **PktPrivacy** 以進行驗證。 **RequiresEncryption** 限定詞會讓 WMI 拒絕任何傳入的資料要求，除非它們明確地使用加密的驗證。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md) 或 [使用 c + + 設定驗證](setting-authentication-using-c-.md)。

您也可以藉由新增這個屬性來修改現有的命名空間，然後再次編譯 MOF 檔案。 **RequiresEncryption** 可用於具有 [pragma 命名空間](pragma-namespace.md)預處理器指令的 [*MOF*](gloss-m.md)中。

下列程式會將命名空間設定為需要加密的連接。

**設定必要的加密**

1.  建立受控物件格式 (MOF) 檔，或修改現有的 MOF 檔案來定義命名空間。

    下列程式碼範例會示範要修改的命名空間是 *根 \\ MyNamespace* ，而檔案名為 *MyNamespace \_ security. mof*。 **RequiresEncryption** 具有布林資料類型，因此必須設定為 **True** 或 **False**。

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  執行 [**mofcomp.exe**](mofcomp.md) 以編譯 MOF 檔案。

    **c： \\ Mofcomp.exe MyNamespace \_ security. mof**

    在 c + + 中，請使用 [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 方法。

WMI 會拒絕使用預設驗證層級的用戶端，因為 DCOM 會將安全性協調為執行 WMI 服務的 SVCHOST 進程所需的層級。 如需服務主機的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。 如需有關連接到 WMI 命名空間時設定驗證層級的詳細資訊，請參閱使用 [c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md)、使用 [c + + 設定驗證](setting-authentication-using-c-.md)，或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

在非同步回呼連接上傳回資料時，WMI 會將拒絕存取的訊息傳回給提出要求的電腦。 WMI 也會使用加密的命名空間，在電腦的 NT 事件記錄檔中建立記錄專案，表示無法建立用戶端的安全連線。

從 Windows Vista 開始，WbemCore 檔案已不再存在。 您可以檢查 NT 事件記錄檔中的專案，指出已拒絕需要加密的命名空間的輸入資料要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



