---
description: 關聯提供者會提供一種機制來註冊設定檔，並將其與在不同命名空間中執行的設定檔產生關聯。
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: 撰寫 Interop 的關聯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ef4e73c35c942e56b2636b7fced4c7e468e120
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887436"
---
# <a name="writing-an-association-provider-for-interop"></a>撰寫 Interop 的關聯提供者

關聯提供者會提供一種機制來註冊設定檔，並將其與在不同命名空間中執行的設定檔產生關聯。

關聯提供者可用來公開標準設定檔，例如電源設定檔。 這是藉由在根/interop 命名空間中撰寫關聯提供者來完成，此命名空間會衍生自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))的類別，以公開關聯實例。 提供者必須在根/interop 和根/實命名空間中註冊 &lt; &gt; ，才能支援跨命名空間的遍歷。

Windows每當在根/interop 命名空間中執行關聯查詢時，Management Instrumentation (WMI) 就會載入關聯提供者。

**若要執行 interop 的關聯提供者**

1.  從 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 衍生類別，並在根 \\ interop 命名空間中建立此衍生類別的靜態實例。 下列屬性至少必須以有效的值傳播：

    -   [**Id**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    即使 [**InstanceID**](/previous-versions//ee309375(v=vs.85)) 可唯一定義 **CIM \_ RegisteredProfile** 的實例， **RegisteredName**、 **RegisteredOrganization** 和 **RegisteredVersion** 的組合也必須在組織的範圍內唯一識別已註冊的設定檔。 如需個別屬性的詳細資訊，請參閱 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

    下列程式碼範例說明從 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))衍生 **ProcessProfile** 類別以及擴展靜態實例的語法。

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > 針對 Windows 用戶端， **RegisteredOrganization** 屬性必須設定為1，而且 **OtherRegisteredOrganization** 屬性設定為 "Microsoft"。

     

2.  建立可傳回 [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)關聯實例的提供者。 這項處理序有兩個步驟。

    1.  建立衍生自 interop 和執行命名空間中 [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) 的類別。 因為相同的設定檔可以由不同的廠商來執行，所以類別的名稱應該是唯一的。 建議的命名慣例為 " &lt; Organization &gt; \_ &lt; ProductName &gt; \_ &lt; ClassName &gt; \_ &lt; Version &gt; "。 **ConformantStandard** 或 **ManagedElement** 屬性必須指定包含這個類別所屬之命名空間的 **MSFT \_ TargetNamespace** 限定詞。

        下列程式碼範例說明 \_ \_ \_ 從根 interop 命名空間中的 [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) 衍生 Microsoft Process ElementConformsToProfile v1 類別的語法 \\ 。 在此範例中，Win32 \_ 進程 managed 元素會 \\ 使用 **MSFT \_ TargetNamespace** 辨識符號來參考根 cimv2 命名空間。

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        下列程式碼範例說明 \_ \_ \_ 從根 cimv2 命名空間中的 [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) 衍生 Microsoft Process ElementConformsToProfile v1 類別的語法 \\ 。 在此範例中， [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 一致標準會 \\ 使用 **MSFT \_ TargetNamespace** 辨識符號來參考根 interop 命名空間。

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        如果未在參考已實命名空間的屬性上指定 **MSFT \_ TargetNamespace** 限定詞，則 "associators of of" 語句的 **ResultClass** 篩選器將無法運作。 例如，如果未指定 **MSFT \_ TargetNamespace** 辨識符號，下列 Windows PowerShell 命令列將不會傳回物件： **>get-wmiobject-query "associators of of {ProcessProfile. InstanceID = ' Process '} where resultclass = ' Win32 \_ Process '"**。

        **MSFT \_ TargetNamespace** 辨識符號無法指向遠端電腦上的命名空間。 例如，不支援下列命名空間： MSFT \_ TargetNamespace (\\ \\ \\ \\ &lt; RemoteMachine &gt; \\ \\ 根 \\ \\ interop) 。

    2.  撰寫提供者，以傳回所建立之衍生類別的實例。 如需詳細資訊，請參閱 [撰寫執行個體提供者](writing-an-instance-provider.md)。 當您存取跨命名空間實例時，可能需要存取用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

        關聯提供者應該同時執行 [**iwbemservices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) 和 [**iwbemservices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法。 執行 [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法是選擇性的。 因為此提供者可以從根 \\ interop 和根實 \\ &lt; 命名空間進行存取 &gt; ，所以不應該對提供者內的命名空間有明確的相依性。

3.  在根 \\ interop 和根 \\ &lt; 執行的 &gt; 命名空間中註冊關聯提供者。 如需詳細資訊，請參閱 [註冊執行個體提供者](registering-an-instance-provider.md)。

    下列程式碼範例說明在根 interop 命名空間中註冊關聯提供者的語法 \\ 。

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    下列程式碼範例說明在根 cimv2 命名空間中註冊關聯提供者的語法 \\ 。

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  將 [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) 的架構放入已執行的命名空間中。 針對 Windows 用戶端，這是位於% systemroot% \\ system32 wbem 資料夾中的 interop. mof 檔案 \\ 。
5.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。 [**IWbemProviderInit.Ini的 tialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)方法應該以允許對兩個不同命名空間呼叫的方式來執行。 如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[撰寫執行個體提供者](writing-an-instance-provider.md)
</dt> <dt>

[註冊執行個體提供者](registering-an-instance-provider.md)
</dt> </dl>

 

 
