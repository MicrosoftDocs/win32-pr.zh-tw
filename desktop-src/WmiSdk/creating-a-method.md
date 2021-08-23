---
description: 若要建立 WMI 方法，請定義方法的輸入和輸出參數。
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: 建立 WMI 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689f69518f440e7c1983a92fbf86877c5c6dd2149ce2b31b8459aa08b9e94c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612528"
---
# <a name="creating-a-wmi-method"></a>建立 WMI 方法

若要建立 WMI 方法，請定義方法的輸入和輸出參數。 輸入和輸出參數是由特殊的 WMI 系統類別 [**\_ \_ 參數**](--parameters.md)表示。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [撰寫方法提供者](writing-a-method-provider.md)。

本主題將討論下列各節：

-   [在 MOF 中建立 WMI 類別方法](#creating-a-wmi-class-method-in-mof)
-   [在 c + + 中建立 WMI 類別方法](#creating-a-wmi-class-method-in-c)
-   [相關主題](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>在 MOF 中建立 WMI 類別方法

在 WMI 中，提供者方法通常是與類別所表示之物件相關的不同動作。 應該建立方法，而不是變更屬性的值來執行動作。 例如，您可以使用 [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter)和 [**disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter)方法，啟用或停用 [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)所代表的網路資訊中心 (NIC) 。 雖然這些動作可以表示為讀取/寫入屬性，但建議的設計是建立方法。 或者，如果您想要讓類別能看到狀態或值，則建議的方法是建立讀取/寫入屬性，而不是方法。 在 **Win32 \_ NetworkAdapter** 中， **NetEnabled** 屬性會讓介面卡的狀態成為可見的，但狀態之間的變更會由 **Enable** 或 **Disable** 方法執行。

類別宣告可以包含一或多個方法的宣告。 您可以選擇繼承父類別的方法，或執行您自己的方法。 如果您選擇執行自己的方法，您必須宣告方法，並使用特定的辨識符號標記來標記方法。

下列程式描述如何在不繼承自基類的類別中宣告方法。

**宣告方法**

1.  在類別宣告的大括弧之間定義方法的名稱，後面加上任何限定詞。

    下列程式碼範例描述方法的語法。

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  完成之後，請呼叫 MOF 編譯器，將受控物件格式 (MOF) 程式碼插入 WMI 存放庫中。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

下列清單會定義方法宣告的元素。

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**供應商**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

將特定提供者連結至您的類別描述。 [**提供**](/windows/desktop/api/Provider/nl-provider-provider)者辨識符號的值是提供者的名稱，它會告知 WMI 支援您方法的程式碼所在位置。 提供者也應使用 **動態** 辨識符號來標記具有動態實例的任何類別。 相反地，請勿使用 **動態** 辨識符號來標記包含具有已 **執行** 方法之靜態實例的類別。

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**實現**
</dt> <dd>

宣告您將會執行方法，而不是從父類別繼承方法執行。 根據預設，WMI 會將父類別的執行傳播至衍生類別，除非衍生的類別提供實值。 省略實 **辨識符號表示** 方法在該類別中沒有任何實作為。 如果您在沒有已實辨識 **符號的** 情況下重新宣告方法，WMI 仍會假設您不會執行該方法，並在呼叫時叫用父類別方法執行。 因此，在衍生類別中重新宣告方法，但不附加已 **實限定詞，** 則只有在您于方法中加入或移除辨識符號時才有用。

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

說明方法傳回的值。 方法的傳回值必須是布林值、數值、 **CHAR**、 **字串**、 [日期時間](datetime.md)或架構物件。 您也可以將傳回類型宣告為 [VOID](void.md)，表示該方法不會傳回任何內容。 不過，您不能將陣列宣告為傳回值型別。

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

定義方法的名稱。 每個方法都必須有唯一的名稱。 WMI 不允許在一個類別或類別階層中，有兩個相同名稱和不同簽章的方法存在。 因此，您也不能多載方法。

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

包含描述參數為輸入參數、輸出參數或兩者的限定詞。 請勿使用相同的參數名稱做為輸入參數，或使用一次以上作為輸出參數。 如果相同的參數名稱同時出現 [**在 in**](standard-qualifiers.md) 和 **out** 限定詞中，則此功能在概念上與在單一參數上使用 **in**、 **Out** 限定詞相同。 不過，當使用不同的宣告時，輸入和輸出參數在其他所有方面都必須完全相同，包括 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號的數目和類型，而且限定詞必須相同且明確地針對兩者宣告。 強烈建議您在單一參數宣告中使用 **In**、 **Out** 限定詞。

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

包含 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號，可唯一識別方法中參數序列內每個參數的位置。 根據預設，MOF 編譯器會自動以 **識別碼** 限定詞標記參數。 編譯器會標示值為 0 (零) 的第一個參數，第二個參數的值為 1 (一個) 等等。 如有必要，您可以在 MOF 程式碼中明確陳述識別碼序列。

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

描述方法可接受的資料類型。 您可以將參數類型定義為任何 MOF 資料值，包括陣列、架構物件或參考。 使用陣列做為參數時，請使用陣列做為未系結或明確的大小。

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

包含參數的名稱。 您也可以選擇在此時定義參數的預設值。 缺少初始值的參數會維持未指派狀態。

</dd> </dl>

下列程式碼範例描述參數清單和限定詞。

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

下列程式碼範例說明如何使用 MOF 參數中的陣列。

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

下列程式碼範例說明如何使用架構物件做為參數和傳回值。

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

下列程式碼範例描述如何包含兩個參考：一個用於 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例，另一個則是未知物件類型的實例。

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a>在 c + + 中建立 WMI 類別方法

下列程式描述如何以程式設計方式建立 WMI 類別方法。

**以程式設計方式建立 WMI 類別方法**

1.  建立方法將所屬的類別。

    在建立方法之前，您必須先有一個可將方法放在其中的類別。

2.  使用 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)或 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出 [**\_ \_ PARAMETERS**](--parameters.md)系統類別的兩個子類別。

    您可以使用第一個子類別來描述 in 參數，並使用第二個子類別來描述 out 參數。 如有必要，您可以執行單一抓取，然後呼叫 [**IWbemClassObject：： Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) 方法。

3.  使用一或多個 IWbemClassObject 呼叫，將 in 參數寫入第一個類別，並將 out 參數寫入至第二個類別 [**：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)。

    描述方法的參數時，請遵守下列規則和限制：

    -   將 \[ in、out \] 參數視為個別的專案，其中一個在包含 in 參數的物件中，另一個在包含 out 參數的物件中。
    -   除了 \[ in、out 限定詞之外 \] ，其餘的限定詞必須完全相同。
    -   指定 [**識別碼**](standard-wmi-qualifiers.md) 限定詞，從 0 (零) 開始，每個參數一個。

        輸入或輸出參數的順序，是由每個參數上的 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號值所建立。 所有輸入引數都必須在任何輸出引數之前。 在更新現有的方法提供者時，變更方法輸入和輸出參數的順序，可能會導致呼叫方法的應用程式失敗。 在現有參數的結尾加入新的輸入參數，而不是以已經建立的順序來插入。

        請務必不要在 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號序列中保留任何間距。

    -   將傳回值放在 out 參數類別中，作為名為 **ReturnValue** 的屬性。

        這會將屬性識別為方法的傳回值。 這個屬性的 CIM 型別是方法的傳回型別。 如果方法的傳回型別為 void，則完全沒有 **ReturnValue** 屬性。 此外， **ReturnValue** 屬性不能有與方法的引數類似的 [**識別碼**](standard-wmi-qualifiers.md) 限定詞。 將 **識別碼** 辨識符號指派給 **ReturnValue** 屬性會產生 WMI 錯誤。

    -   表示類別中屬性的任何預設參數值。

4.  呼叫 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)，將這兩個 [**\_ \_ 參數**](--parameters.md)物件放在父類別中。

    對 [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)的單一呼叫可以將這兩個 [**\_ \_ 參數**](--parameters.md)物件放入類別中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類別](creating-a-class.md)
</dt> </dl>

 

 
