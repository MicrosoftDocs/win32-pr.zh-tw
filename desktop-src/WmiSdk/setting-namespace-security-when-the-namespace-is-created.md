---
title: 設定命名空間建立時的安全性
description: 建立命名空間的受控物件格式 (MOF) 檔也可以定義命名空間的安全描述項，方法是將 NamespaceSecuritySDDL 限定詞包含在安全描述項定義語言 (SDDL) 格式的安全描述項中。
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514085"
---
# <a name="setting-security-on-namespace-creation"></a>設定命名空間建立時的安全性

建立命名空間的受控物件格式 (MOF) 檔也可以定義命名空間的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) ，方法是將 **NamespaceSecuritySDDL** 限定詞包含在 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 格式的安全描述項中。

您可以使用 **NamespaceSecuritySDDL** 來保護任何命名空間。 您也可以在簡單的 MOF 檔案中使用這個辨識符號，以改變現有命名空間的安全描述項。 SDDL 字串是由 WMI 處理來建立命名空間安全性，但不會儲存為字串。 如果未指定任何安全描述項，則會使用預設安全性。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

下列程式會設定 *根 \\ MyNamespace* 命名空間的安全描述項。 SDDL 字串會將擁有者和群組設定為已驗證的使用者，並指定子命名空間繼承 [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 。 DACL 可讓使用者讀取資料、執行方法、將資料寫入提供者類別，以及使用遠端存取： **wbem \_ 啟用**、 **wbem \_ 方法 \_ 執行**、 **wbem \_ 寫入 \_ 提供者**、 **wbem \_ 遠端 \_ 訪問**。 如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。

**設定命名空間 DACL**

1.  建立受控物件格式 (MOF) 檔或修改現有的 MOF 檔案，該檔案會定義命名空間，以使用 SDDL 字串來新增 **NamespaceSecuritySDDL** 限定詞。

    下列程式碼範例顯示要修改的命名空間是根 \\ MyNamespace，而檔案的名稱為 MyNamespace \_ security. mof。

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  請注意，SDDL 字串會區分大小寫：字母必須為大寫。

    下列程式碼範例會將 SDDL 字串中的字母 "o" 和 "g" 顯示為小寫，而且會導致 Mofcomp.exe 傳回錯誤。

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  執行 [**Mofcomp.exe**](mofcomp.md) 以編譯 MOF 檔案。

    **c： \\ Mofcomp.exe MyNamespace \_ security. mof**

    在 c + + 中，請使用 [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 方法。

4.  如果您嘗試設定命名空間 DACL 失敗，請考慮下列錯誤訊息：

    

    | 錯誤                           | 描述                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **WBEM \_ E \_ 不正確 \_ 參數** | 沒有繼承的 DACL。 或者，呼叫端違反了父命名空間中的 DACL 或 SD。 |
    | **WBEM \_ E \_ \_ 拒絕存取**     | 呼叫端沒有在 MOF 中更新 SDDL 的許可權。                                               |

    

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[**命名空間存取權限常數**](namespace-access-rights-constants.md)
</dt> <dt>

[**命名空間 ACE 旗標常數**](namespace-ace-flag-constants.md)
</dt> <dt>

[變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
