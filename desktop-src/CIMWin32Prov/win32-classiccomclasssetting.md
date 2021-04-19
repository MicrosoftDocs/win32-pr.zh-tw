---
description: 表示元件物件模型 (COM) 元件的設定。
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970539"
---
# <a name="win32_classiccomclasssetting-class"></a>Win32 \_ ClassicCOMClassSetting 類別

**Win32 \_ ClassicCOMClassSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表元件物件模型 (COM) 元件的設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>成員

**Win32 \_ ClassicCOMClassSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ClassicCOMClassSetting** 類別具有這些屬性。

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] " ) 
</dt> </dl>

全域唯一識別碼 (使用此 COM 元件之 COM 應用程式的 GUID) 。

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ Default \] " ) 
</dt> </dl>

將自動轉換此 COM 元件之 COM 類別的 GUID。

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs \[ Default \] " ) 
</dt> </dl>

將自動模擬這個類別之實例的 COM 元件的 GUID。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ Default \] " ) 
</dt> </dl>

此 COM 元件的 GUID。

</dd> <dt>

**控制**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Control" ) 
</dt> </dl>

COM 元件是一個 OLE 控制項。

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ Default \] " ) 
</dt> </dl>

可執行檔的路徑，以及類別使用之預設圖示的資源識別碼。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ Default \] " ) 
</dt> </dl>

COM 元件之16位自訂處理常式的完整路徑，包括檔案名或僅檔案名。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] " ) 
</dt> </dl>

COM 元件之32位自訂處理常式的完整路徑，包括檔案名或僅檔案名。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ Default \] " ) 
</dt> </dl>

此 COM 元件的完整路徑（包含檔案名或僅檔案名）至16位同進程伺服器 DLL。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ Default \] " ) 
</dt> </dl>

此 COM 元件的完整路徑（包含檔案名）或僅限32位同進程伺服器 DLL 的檔案名。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**插入**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} 「 \\ \\ 插入」 ) 
</dt> </dl>

COM 元件可以插入至 OLE 容器應用程式。

</dd> <dt>

**JAVAClass**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JAVAClass \] " ) 
</dt> </dl>

COM 元件是 JAVA 元件。

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ Default \] " ) 
</dt> </dl>

完整路徑（包括檔案名），或只包含檔案名至16位本機伺服器應用程式。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ Default \] " ) 
</dt> </dl>

包含檔案名的完整路徑，或僅限32位本機伺服器應用程式的檔案名。 提供者不一定會傳回完整的路徑。

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ Default \] " ) 
</dt> </dl>

COM 應用程式的完整名稱。 它會用於 [ **OLE 貼上特殊**] 對話方塊的 [**結果**] 欄位等區域中。

</dd> <dt>

**ProgId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ Default \] " ) 
</dt> </dl>

與 COM 元件相關聯的程式設計識別碼。 ProgID 的格式是 <廠商. <元件。 <版本。 此識別碼不保證是唯一的。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ Default \] " ) 
</dt> </dl>

 (在功能表和快顯) 中使用的 COM 應用程式的簡短名稱。

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ >threadingmodel \] " ) 
</dt> </dl>

同進程 COM 類別所使用的執行緒模型。 如果此屬性為 **Null**，則不會使用任何執行緒模型。 元件是在用戶端的主執行緒上建立，而來自其他執行緒的呼叫會封送處理至此執行緒。

單元模型指定元件只能由一個執行緒輸入。 這些類型的物件服務器所保留的一般資料必須受到保護，以免執行緒衝突，因為物件服務器支援多個元件。 不同的執行緒可以同時輸入每個元件。

免費模型指定元件對哪些執行緒或可輸入物件的執行緒沒有任何限制。 物件不能包含執行緒特定的資料，而且必須保護其資料，使其無法同時存取多個執行緒。 但是，無限制執行緒元件無法直接由單元執行緒存取，而且它們的呼叫會從用戶端單元封送處理。

當兩者都指定時，元件可用於單元執行緒或無線程模式。 這些元件可以由多個執行緒輸入、保護其資料免于執行緒衝突，且不包含執行緒特定資料。

值如下：

<dl> <dd>Apartment</dd> <dd>存在</dd> <dd>對</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**公寓** ( 「單元」 ) 


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**免費** ( 「免費」 ) 


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**兩者都** ( 「兩者」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] " ) 
</dt> </dl>

適用于 [工具列] 或 [工具箱] 按鈕臉部的小型 (16x16) 點陣圖的模組名稱和資源識別碼。 當 COM 元件是 OLE 或 ActiveX 控制項時使用。

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ Default \] " ) 
</dt> </dl>

可以模擬此元件之實例的 COM 元件的 GUID。

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ Default \] " ) 
</dt> </dl>

此 COM 元件之類型程式庫的 GUID。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Version \[ Default \] " ) 
</dt> </dl>

這個 COM 類別的版本號碼。

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ Default \] " ) 
</dt> </dl>

相同程式的所有版本都是一致的程式識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ ClassicCOMClassSetting** 類別衍生自 [**win32 \_ COMSetting**](win32-comsetting.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ COMSetting**](win32-comsetting.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

