---
description: 以下列出 WMI 特定的標準限定詞。
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: 標準 WMI 限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cfcd600bd539cbe17dad3d7a9c66bf27679618427665a6fd06e8a9a69a4ea5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383558"
---
# <a name="standard-wmi-qualifiers"></a>標準 WMI 限定詞

以下列出 WMI 特定的標準限定詞。

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**修訂**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指出類別包含已修改的修飾限定詞。 預設值為 **TRUE**。

可以轉譯相關聯的類別。 若要存取翻譯的版本，請使用地區設定識別碼來建立命名空間名稱。

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**略過 \_ GetObject**
</dt> <dd>

資料類型： **布林值**

適用于：方法

指出方法呼叫應該直接傳遞給提供者的 **ExecMethodAsync** 呼叫，而不是提供者先對 **GetObject** 進行呼叫，以驗證物件路徑。 預設值為 **FALSE**。 使用 **略過 \_ GetObject** 可大幅提升效能。

使用「 **略過 \_ GetObject**」之前，請確定不會採取下列動作：

-   從您的類別衍生類別。
-   覆寫具有 **略過 \_ GetObject** 辨識符號的方法。

若無法遵循這些預防措施，可能會導致叫用父類別的方法執行，而不是子類別。 如需詳細資訊，請參閱使用略過 \_ GetObject 限定詞。

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM \_ 金鑰**
</dt> <dd>

資料類型： **CIM \_ 布林值**

適用物件：屬性

指出相關聯的屬性是 CIM 中的索引鍵屬性，但不是 WMI 中的索引鍵屬性。

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)
</dt> <dd>

資料類型： **VT \_ BSTR**

適用物件：屬性、方法、參數

包含描述屬性類型的文字。

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassCoNtext**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用于：類別

指出類別具有與提供者動態提供的詳細資訊相關聯的實例。

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**廢棄**
</dt> <dd>

資料類型： **CIM \_ 布林值**

適用物件：屬性、類別

表示屬性已由另一個屬性取代。

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**顯示**
</dt> <dd>

適用于：類別、屬性

相關聯類別的 **UUID** 。

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**動態**](dynamic-qualifier.md)
</dt> <dd>

資料類型： **布林值**

適用于：類別、屬性

表示以動態方式建立實例的類別。 此限定詞的值必須設定為 **TRUE**。

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**
</dt> <dd>

資料類型： **布林值**

適用于：類別、實例

指出實例包含動態屬性提供者所提供的值。 預設值為 **TRUE**。

您必須在這類實例上指定這個限定詞。 只允許值 **TRUE** 。

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**固定**
</dt> <dd>

資料類型： **CIM \_ 布林值**

適用于：實例

指出這個屬性的值在實例的存留期內無法變更。

</dd> <dt>

<span id="ID"></span><span id="id"></span>**Id**
</dt> <dd>

資料類型： **VT \_ I4**

適用物件：屬性、參數

當自動產生 MOF 語句時，可唯一識別和序列屬性或方法參數。

只有方法參數需要此限定詞。 建立方法的參數時，類別設計工具的開頭應該是第一個參數的識別碼 (0) ，然後針對每個後續的參數使用每個後續的整數。 如果未小心省略 **識別碼** 限定詞，MOF 編譯器會自動產生 **識別碼** 限定詞。

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**實現**
</dt> <dd>

資料類型： **布林值**

適用于：方法

指出方法具有提供者所提供的實作為。

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceCoNtext**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用于：實例

指出實例包含動態屬性提供者所提供的值。

值會傳遞給屬性提供者，做為 [**IWbemPropertyProvider：： GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 方法的引數。

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**現場**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用于：類別或實例

指定類別或實例的原始語言。 如需地區設定值的詳細資訊，請參閱 [地區設定代碼](#locale-codes)。

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**
</dt> <dd>

資料類型： **字串陣列**

適用于：命名空間實例

以 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 格式指定命名空間的安全描述項。 如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。 SDDL 字串是由 WMI 處理來建立命名空間安全性，但不會儲存為字串。 如果未指定任何安全描述項，則會使用預設安全性。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**選**
</dt> <dd>

資料類型： **布林值**

適用于：參數

表示不需要參數，且其具有行為良好的預設值。

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**特權**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性、方法

值的集合，用來通知用戶端建立實例、填入屬性或執行方法時需要哪些許可權。 預設值為 **FALSE**。

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyCoNtext**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用物件：屬性

指出實例屬性包含動態屬性提供者所提供的值。

您必須在這類屬性上指定這個限定詞。 值會以引數形式傳遞給屬性提供者，以作為 [**IWbemPropertyProvider：： GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty)的引數。

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用于：類別

此辨識符號的值是提供類別實例和重新整理實例資料的動態提供者名稱。 您必須使用包含此名稱的 **name** 屬性來建立 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例，以向 WMI 註冊此名稱。 當此限定詞指定于動態提供其實例的類別上時，也必須指定 **動態** 限定詞。

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**
</dt> <dd>

資料類型： **布林值**

適用于：命名空間實例

如果設定為 **TRUE**， **RequiresEncryption** 會標示命名空間，讓用戶端應用程式和腳本必須使用加密的驗證進行連接。 驗證層級必須設定為 c + + 中的 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 。 在腳本或 Visual Basic 中，驗證層級必須設為 **WbemAuthenticationLevelPktPrivacy**。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。 辨識符號是用於具有 pragma 命名空間預處理器命令的 [*MOF*](gloss-m.md) 中。

如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md) 或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。 腳本驗證層級是在 [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)中定義。

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**單身 人士**
</dt> <dd>

資料類型： **布林值**

適用于：類別

指定只能有一個實例而且不包含索引鍵屬性的類別。

只允許值 **TRUE** (預設) 。

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**靜態**
</dt> <dd>

資料類型： **布林值**

適用于：方法

指出方法是否可以使用類別定義或其實例來呼叫。

無法從實例叫用方法。

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**亞**
</dt> <dd>

資料類型： **VT \_ BSTR**

適用物件：屬性

指出 **CIM \_ DATETIME** 類型的屬性代表時間間隔，而不是特定時間。

若要將屬性識別為間隔，此限定詞的值必須是 "interval"。 此辨識符號的所有其他值都會保留供日後使用。

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**Uuid**
</dt> <dd>

資料類型： **字串**

適用于：類別

套用至類別的通用唯一識別碼。

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**
</dt> <dd>

資料類型： **字串**

適用于：類別

類別物件的版本號碼。 預設值為 **Null**。 當對類別進行變更時，版本號碼會遞增。

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**
</dt> <dd>

資料類型： **字串陣列**

適用物件：屬性

值的集合，指出哪些系統許可權必須可供使用且已啟用，以進行成功的寫入操作。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="locale-codes"></a>地區設定代碼

地區設定代碼的格式為 "MS \_ <Three Digit Language ID> "。 例如，英文地區設定為 MS \_ 409。 下表列出語言識別項。



| 語言              | 語言識別項 (十六進位)  |
|-----------------------|---------------------------|
| 阿拉伯文                | 401                       |
| 葡萄牙文 (巴西)   | 416                       |
| 簡體中文  | 804                       |
| 繁體中文 | 404                       |
| 捷克文                 | 405                       |
| 丹麥文                | 406                       |
| 荷蘭文                 | 413                       |
| 英文 (預設值)     | 409                       |
| 芬蘭文               | 40b                       |
| 法文                | 40c                       |
| 德文                | 407                       |
| 希臘文                 | 408                       |
| Hebrew                | 40d                       |
| 匈牙利文             | 40e                       |
| 義大利文               | 410                       |
| 日文              | 411                       |
| 韓文                | 412                       |
| 挪威文             | 414                       |
| 波蘭文                | 415                       |
| 葡萄牙文 (葡萄牙) | 816                       |
| 俄文               | 419                       |
| 西班牙文               | c0a                       |
| 瑞典文               | 41D                       |
| 土耳其文               | 41f                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>使用略過 \_ GetObject 辨識符號

在方法上使用 **略過 \_ GetObject** 限定詞可能會產生令人困惑的結果。

下列範例會定義 **圖形** 和 **圓形** 類別。 請注意， **圓形** 類別衍生自 **Shape** 類別。


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



下列對 **ExecMethod** 的呼叫會使用名為 "MyCircle" 的 **圓形** 物件來繪製圓形。


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



在先前的案例中，WMI 會呼叫 **GetObject**;探索 "Shape. Name = ' MyCircle '" 是 **圓形**;並執行 **DrawIt** 的 **圓形** 實作為。 但是，如果您在 **DrawIt** 上使用 [**略過 \_ getobject** 辨識符號]，WMI 不會呼叫 **GetObject**，而不會發現 "shape. Name = ' MyCircle '" 是 **圓形**，而是執行 **DrawIt** 的 **圖形** 實，而不是 **DrawIt** 的 **圓形** 實作為。

下列 **ExecMethod** 呼叫一律會叫用正確的 **DrawIt** 執行。


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[WMI 限定詞](wmi-qualifiers.md)
</dt> <dt>

[新增限定詞](adding-a-qualifier.md)
</dt> </dl>

 

