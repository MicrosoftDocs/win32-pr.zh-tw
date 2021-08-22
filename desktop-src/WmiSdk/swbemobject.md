---
description: 您可以使用 SWbemObject 物件的方法和屬性，來代表 (WMI) 類別定義或物件實例的一個 Windows Management Instrumentation。
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: 'SWbemObject 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f8e33a3a0a5028292ce7cef7b44a37433b00f942ea9459ec18e6d53e1cf9a43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504048"
---
# <a name="swbemobject-object"></a>SWbemObject 物件

您可以使用 **SWbemObject** 物件的方法和屬性，來代表 (WMI) 類別定義或物件實例的一個 Windows Management Instrumentation。 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。

此物件支援兩種類型的屬性和方法。 本節中定義的屬性是套用至所有 WMI 物件的一般屬性和方法。 此外，這個物件會公開基礎物件的屬性和方法，作為動態 automation 屬性和 **SWbemObject** 的方法。 這些屬性和方法的名稱和類型相依于基礎 WMI 物件。 如需如何公開這些動態屬性和方法的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

從 WMI 用戶端的觀點來看，這個物件永遠都是同進程。 寫入作業只會影響物件的本機複本，而讀取作業一律會從本機複本取出值。 只有在使用 [**SWbemObject \_**](swbemobject-put-.md)的呼叫來寫入整個物件時，才會執行 WMI 的更新。 如果您修改 **SWbemObject** 物件中的屬性或方法，則在呼叫 **SWbemObject \_** 之前，您的變更不會寫入至 WMI。

此區段中定義的泛型方法和屬性名稱一律以尾端底線結尾 ( " \_ " ) 來區別它們與基礎物件的動態 WMI 方法和屬性。

請注意， **SWbemObject** 無法使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). 方法來建立。 如果您想要建立新的空白類別，請使用 [**SWbemServices。 Get**](swbemservices-get.md) 具有空的 path 參數。 此呼叫會傳回空的 **SWbemObject** 物件，該物件可以成為類別。 然後，您可以為 [**\_ 路徑**](swbemobject-path-.md)呼叫所傳回之 [**SWbemObjectPath**](swbemobjectpath.md)物件的 [**class**](swbemobjectpath-class.md)屬性提供類別名稱。 由 [**properties \_**](swbemobject-properties-.md)方法將屬性加入至新的類別。 若要建立實例，請在新類別上呼叫 **GetObject** 。

下列程式碼範例示範如何取得新的類別，並在其中加入屬性。 代表類別的 **SWbemObject** 物件必須透過呼叫 Put 寫回至 WMI [**存放 \_**](swbemobject-put-.md)庫。


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



您可以使用 [CIM Studio](further-information.md) 之類的查看工具來檢查存放庫，以確認新的類別和實例出現。 如需從存放庫中移除類別和實例的範例，請參閱 [**SWbemServices。刪除**](swbemservices-delete.md)或 [**\_ SWbemObject。**](swbemobject-delete-.md)

## <a name="members"></a>成員

**SWbemObject** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemObject** 物件有這些方法。



| 方法                                                        | 描述                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Associators of\_**](swbemobject-associators-.md)             | 抓取物件的 associators of。<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | 以非同步方式抓取物件的 associators of。<br/>                                      |
| [**複製\_**](swbemobject-clone-.md)                         | 建立目前物件的複本。<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | 測試兩個物件是否相等。<br/>                                                              |
| [**刪除\_**](swbemobject-delete-.md)                       | 從 WMI 刪除物件。<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | 以非同步方式從 WMI 刪除物件。<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | 執行方法提供者所匯出的方法。<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | 以非同步方式執行方法提供者所匯出的方法。<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | 抓取物件 (MOF 語法) 的文字標記法。<br/>                             |
| [**執行個體\_**](swbemobject-instances-.md)                 | 傳回物件的實例集合， (必須是) 的 WMI 類別。<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | 以非同步方式傳回物件的實例集合 (必須是 WMI 類別) 。<br/>  |
| [**把\_**](swbemobject-put-.md)                             | 在 WMI 中建立或更新物件。<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | 在 WMI 中以非同步方式建立或更新物件。<br/>                                         |
| [**參考資料\_**](swbemobject-references-.md)               | 傳回物件的參考。<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | 以非同步方式傳回物件的參考。<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | 從目前物件建立新的衍生類別， (必須是) 的 WMI 類別。<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | 從目前的物件建立新的實例。<br/>                                              |
| [**子\_**](swbemobject-subclasses-.md)               | 傳回物件的子類別集合 (必須是) 的 WMI 類別。<br/>                |
| [**SubclassesAsync\_**](swbemobject-subclassesasync-.md)     | 以非同步方式傳回物件的子類別集合 (必須是) 的 WMI 類別。<br/> |



 

### <a name="properties"></a>屬性

**SWbemObject** 物件具有這些屬性。



| 屬性                                                   | 存取類型          | 描述                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**衍生\_**](swbemobject-derivation-.md)<br/> | 唯讀<br/> | 包含描述類別之衍生階層的字串陣列。<br/>                                             |
| [**方法\_**](swbemobject-methods-.md)<br/>       | 唯讀<br/> | [**SWbemMethodSet**](swbemmethodset.md)物件，此物件為這個物件的方法集合。<br/>                           |
| [**路徑\_**](swbemobject-path-.md)<br/>             | 唯讀<br/> | 包含 [**SWbemObjectPath**](swbemobjectpath.md) 物件，該物件表示目前類別或實例的物件路徑。<br/> |
| [**屬性\_**](swbemobject-properties-.md)<br/> | 唯讀<br/> | [**內含**](swbempropertyset.md)物件，此物件為這個物件的屬性集合。<br/>                    |
| [**限定詞\_**](swbemobject-qualifiers-.md)<br/> | 唯讀<br/> | [**SWbemQualifierSet**](swbemqualifierset.md)物件，此物件為這個物件的限定詞集合。<br/>                  |
| [**安全性\_**](swbemobject-security-.md)<br/>     | 唯讀<br/> | 包含用來讀取或變更安全性設定的 [**SWbemSecurity**](swbemsecurity.md) 物件。<br/>                         |



 

## <a name="examples"></a>範例

這份清單列出了 TechNet 資源庫上 WMI 類別 VBScript 程式碼範例的 [所有屬性和方法](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) ，會使用 SWbemObject 來列出所指定 WMI 類別的所有方法和屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

