---
description: 在執行提供者之前，您應該先向 WMI 註冊您的提供者。 註冊提供者會定義提供者的類型和提供者支援的類別。 WMI 只能存取已註冊的提供者。
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: 註冊提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265d3a9f8617c68793fc30c0dc23fd3e9f0106ee98a9e3c757754e2fe589dda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995918"
---
# <a name="registering-a-provider"></a>註冊提供者

在執行提供者之前，您應該先向 WMI 註冊您的提供者。 註冊提供者會定義提供者的類型和提供者支援的類別。 WMI 只能存取已註冊的提供者。

> [!Note]  
> 如需註冊 MI 提供者的詳細資訊，請參閱 [如何：註冊 Mi 提供者](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider)。

 

註冊提供者之前，您可以撰寫提供者程式碼。 不過，您很難對未向 WMI 註冊的提供者進行 debug 錯。 判斷您提供者的介面也有助於概述提供者的用途和結構。 因此，註冊您的提供者可協助您設計您的提供者。

只有系統管理員可以註冊或刪除提供者。

提供者必須針對其執行的所有不同類型的提供者函式註冊。 幾乎所有提供者都提供其定義的類別實例，但它們也可以提供屬性資料、方法、事件或類別。 提供者也可以註冊為事件取用者提供者或效能計數器提供者。 建議您將所有提供者功能合併成一個提供者，而不是針對每個類型各有許多不同的提供者。 例如，提供方法和實例的 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)，以及提供實例、方法和事件的 [磁片配額提供者](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)。

提供者必須針對其執行的所有不同類型的提供者函式註冊。 幾乎所有提供者都提供其定義的類別實例，但它們也可以提供屬性資料、方法、事件或類別。 提供者也可以註冊為事件取用者提供者或效能計數器提供者。

每種類型的註冊都使用相同的 [**\_ \_ Win32Provider**](--win32provider.md)實例：

-   [註冊執行個體提供者](registering-an-instance-provider.md)
-   [註冊類別提供者](registering-a-class-provider.md)
-   [註冊方法提供者](registering-a-method-provider.md)
-   [註冊事件提供者](registering-an-event-provider.md)
-   [註冊事件取用者提供者](registering-an-event-consumer-provider.md)
-   [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>範例：建立及註冊提供者的實例

下列範例顯示一個 MOF 檔案，該檔案會在根 cimv2 命名空間中建立並註冊 [System Registry 提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 的實例 \\ 。 它會將別名 $Reg 指派給提供者，以避免在實例和方法註冊中所需的完整路徑名稱。 如需詳細資訊，請參閱 [建立別名](creating-an-alias.md)。

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>範例：註冊提供者

下列程式說明如何註冊提供者。

**註冊提供者**

1.  將提供者註冊為 COM 伺服器。

    如有必要，您可能需要建立登錄專案。 此程式適用于所有的 COM 伺服器，而且與 WMI 無關。 如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 檔中的 COM 一節。

2.  建立 MOF 檔案，其中包含 [**\_ \_ Win32Provider**](--win32provider.md)的實例，以及直接或間接從 [**\_ \_ ProviderRegistration**](--providerregistration.md)（例如 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)）衍生類別的實例。 只有系統管理員可以藉由建立衍生自 **\_ \_ Win32Provider** 或 [**\_ \_ ProviderRegistration**](--providerregistration.md)的類別實例來註冊或刪除提供者。
3.  根據 [裝載模型](provider-hosting-and-security.md)中的值，在 **\_ \_ Win32Provider** 的實例中設定 [**HostingModel**](--win32provider.md) 。

    > [!Note]  
    > 除非提供者需要 LocalSystem 帳戶的高許可權，否則 [**\_ \_ Win32Provider. HostingModel**](--win32provider.md)屬性應設定為 "NetworkServiceHost"。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

     

    下列來自完整範例的 MOF 範例顯示建立 [**\_ \_ Win32Provider**](--win32provider.md)實例的程式碼。

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  直接或間接衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)的類別實例，用來描述提供者的邏輯實作為。 您可以針對數種不同類型的功能來註冊提供者。 上述範例會將 RegProv 註冊為實例和方法提供者。 但是，如果 RegProv 支援此功能，也可以將它註冊為屬性或事件提供者。 下表列出註冊提供者功能的類別。

    

    | 提供者註冊類別                                                        | 描述                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | 註冊 [執行個體提供者](registering-an-instance-provider.md)。             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | 註冊 [事件提供者](registering-an-event-provider.md)。                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | 註冊 [事件取用者提供者](registering-an-event-consumer-provider.md)。 |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | 註冊 [方法提供者](registering-an-event-consumer-provider.md)。          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | 註冊 [屬性提供者](registering-a-property-provider.md)。               |

    

     

5.  將 MOF 檔案放入永久目錄。

    一般而言，您應該將檔案放在提供者的安裝目錄中。

6.  使用 [mofcomp.exe](mofcomp.md) 或 [**IMOFCOMPILER**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯 MOF 檔案。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

    **Windows 8 和 Windows Server 2012：** 當安裝提供者時， [**mofcomp.exe**](mofcomp.md)和 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)介面都會將 \[ 金鑰 \] 和 \[ 靜態 \] 限定詞視為 true （如果存在的話），而不論其實際值為何。 如果有其他限定詞存在但未明確設定為 true，則會將它們視為 false。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> </dl>

 

 
