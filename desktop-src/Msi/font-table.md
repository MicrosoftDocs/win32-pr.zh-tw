---
description: 字型表格包含向系統註冊字型檔案的資訊。
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: 字型資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65efb786d4379bbe14fec0239cd8f3edee50f1b79a6413904b6e00331bc49a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946979"
---
# <a name="font-table"></a>字型資料表

字型表格包含向系統註冊字型檔案的資訊。

字型資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 檔案\_    | [識別碼](identifier.md) | Y   | N        |
| FontTitle | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

字型檔案的檔案 [資料表](file-table.md) 專案中的外部金鑰。 建議包含字型檔案的元件在 \_ [component 資料表](component-table.md)的目錄資料行中指定 FontsFolder。

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

字型名稱。 建議您針對 TrueType 字型和 TrueType 集合將此資料行保留為 null，因為安裝程式可以在從字型檔案讀取正確的字型標題之後註冊字型。 如果輸入字型名稱，它必須與字型檔案中的字型標題相同。 您必須為沒有內嵌名稱的字型指定標題，例如 fon 檔。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [RegisterFonts 動作](registerfonts-action.md) 或 [UnregisterFonts 動作](unregisterfonts-action.md) 時，就會參考此資料表。

如果 [FontTitle] 欄位是空的，則會直接從指定的字型檔案讀取字型名稱。 如果記錄在 FontTitle 欄位中的字型名稱與字型檔案中記錄的內部字型名稱不同，則會使用 [RegisterFonts 動作](registerfonts-action.md)將字型註冊兩次。

字型檔案不能以語言識別項撰寫，因為字型沒有內嵌的語言識別項資源。因此字型檔案的 [語言] 資料 [行應該保留](file-table.md) null。

因為安裝程式預設不會 refcount 字型檔案，所以卸載應用程式時，可能會移除預先存在的字型檔案及其元件。 為了確保不會移除字型檔案，作者可以  \_ \_ \_ 針對包含字型檔案的元件，在元件資料表 msi 元件資料表的 [屬性] 資料行中設定 msidbComponentAttributesSharedDllRefCount 或 msidbComponentAttributesPermanent 位旗標。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



