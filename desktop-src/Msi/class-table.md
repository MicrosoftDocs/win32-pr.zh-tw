---
description: 類別資料表包含必須在產品公告中產生的 COM 伺服器相關資訊。 每個資料列可能會產生一組登錄機碼和值。 此資料表包含相關聯的 ProgId 資訊。
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: 類別資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48985bd2d7e9670c89df53993e7170dc3e0e43a2b6e60f63d29e9f43e8d2ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066038"
---
# <a name="class-table"></a>類別資料表

類別資料表包含必須在產品公告中產生的 COM 伺服器相關資訊。 每個資料列可能會產生一組登錄機碼和值。 此資料表包含相關聯的 ProgId 資訊。

類別資料表具有下列資料行。



| Column           | 類型                         | 答案 | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | Y   | N        |
| Context          | [識別碼](identifier.md) | Y   | N        |
| 元件\_      | [識別碼](identifier.md) | Y   | N        |
| ProgId \_ 預設值  | [Text](text.md)             | N   | Y        |
| 描述      | [Text](text.md)             | N   | Y        |
| AppId\_          | [GUID](guid.md)             | N   | Y        |
| FileTypeMask     | [Text](text.md)             | N   | Y        |
| 圖示\_           | [識別碼](identifier.md) | N   | Y        |
| >iconindex        | [整數](integer.md)       | N   | Y        |
| DefInprocHandler | [檔案名稱](filename.md)     | N   | Y        |
| 引數         | [格式 化](formatted.md)   | N   | Y        |
| 特徵\_        | [識別碼](identifier.md) | N   | N        |
| 屬性       | [整數](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>資料行資訊

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

COM 伺服器 (識別碼) 的類別識別碼。

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>上下文
</dt> <dd>

此伺服器的伺服器內容。 為 CLSID 索引鍵輸入下列其中一個值。



| CLSID 金鑰                             | 描述                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | 指定16位本機伺服器應用程式的完整路徑。             |
| [LocalServer32](../com/localserver32.md)   | 指定32位本機伺服器應用程式的完整路徑。             |
| [InprocServer](../com/inprocserver.md)     | 指定同進程伺服器 DLL 的路徑。                           |
| [InprocServer32](../com/inprocserver32.md) | 指定32位同進程伺服器和執行緒模型的路徑。 |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md) 中，指定金鑰檔提供 COM 伺服器的元件的外部索引鍵。

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ 預設值
</dt> <dd>

與此類別識別碼相關聯的預設程式識別碼。 此資料行是 [ProgID 資料表](progid-table.md)中的外鍵。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

與類別識別碼和程式識別碼相關聯的當地語系化描述。

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_
</dt> <dd>

應用程式識別碼包含相關聯之應用程式的 DCOM 資訊 (字串 [GUID](guid.md)) 。 此資料行是 [AppId 資料表](appid-table.md)中的外鍵。

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

包含此 CLSID) 機碼 (的 HKCR 資訊。

如果有多個模式，則必須以分號分隔，而且會產生數位子機碼：0、1、2 .。。如需此功能的詳細資訊，請參閱 [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile)。

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_
</dt> <dd>

提供與此 CLSID 相關聯之圖示的檔案。 安裝程式會將此資料行中的專案寫入與 ProgId 相關聯的 DefaultIcon 索引鍵下。 如果它不是 null，則資料行是 [圖示資料表](icon-table.md)中的外鍵。 如果是 null，COM 伺服器會提供圖示資源。 宣告的檔案關聯和快捷方式需要此資料行中的非 null 值，才能正確顯示。

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex
</dt> <dd>

圖示檔中的圖示索引。 這個可以是 null。

僅限非負數位。

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

這個欄位會針對內容欄位中指定的伺服器內容，指定預設的同進程處理常式。

如果內容欄位中出現 InprocServer 或 InprocServer CLSID 索引鍵，則這個欄位必須是 Null。

如果 LocalServer 或 LocalServer32 CLSID 索引鍵出現在內容欄位中，則 [DefInprocHandler] 欄位中的值會識別預設的同進程處理常式。



| 值                | 描述                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 非數值    | 安裝程式會將 DefInprocHandler 欄位中的非數值視為系統檔案，做為 InprocHandler32 索引鍵所指定的32位同進程處理常式。                                                                                                            |
| Null                 | LocalServer 或 LocalServer32 CLSID 索引鍵的 DefInprocHandler 和引數欄位都可以是 Null。                                                                                                                                                                           |
| 1 = 預設 (系統)  | 預設值是 InprocHandler 所指定的16位同進程處理常式。 在這種情況下，InprocHandler 的值就是登錄中預設儲存同進程處理常式值的名稱。 例如，HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID。     |
| 2 = 預設 (系統)  | 預設值是 InprocHandler32 所指定的32位同進程處理常式。 在這種情況下，InprocHandler32 的值就是登錄中預設儲存同進程處理常式值的名稱。 例如，HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID。 |
| 3 = 預設 (系統)  | 預設值為16位或32位的同進程處理常式。                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數
</dt> <dd>

如果 LocalServer 或 LocalServer32 CLSID 索引鍵出現在內容欄位中，則此欄位中的文字會註冊為伺服器的引數，並由 COM 用來叫用伺服器。 如果內容欄位中出現 LocalServer 或 LocalServer32，DefInprocHandler 和 Argument 欄位都可以是 Null。

請注意，[引數] 欄位中的屬性解析有限。 \[ \] 當安裝擁有類別的元件時，如果屬性已經有預期的值，則只能解析此欄位中格式化為屬性的屬性。 例如，若要將引數 " \[ \#MyDoc.doc\] " 解析為正確的值，則相同的進程必須安裝 MyDoc.doc 和擁有該類別的元件。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

[功能資料表](feature-table.md)中的外部索引鍵，指定提供 COM 伺服器的功能。

功能資料表的第一個資料行的外部索引鍵。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

如果在此資料行中設定了 **msidbClassAttributesRelativePath** ，則完整檔案名可以用於 COM 伺服器。 安裝程式只會註冊檔案名，而不是完整的路徑。 這可讓目前目錄中的伺服器優先採用，並允許相同元件的多個複本。



| 屬性                            | Decimal | 十六進位 |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [RegisterClassInfo 動作](registerclassinfo-action.md) 或 [UnregisterClassInfo 動作](unregisterclassinfo-action.md) 時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
