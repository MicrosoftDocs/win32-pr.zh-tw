---
description: MsiEmbeddedUI 資料表會定義內嵌在 Windows Installer 套件中的使用者介面。
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: MsiEmbeddedUI 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52846e88e2d8f3edb439aa6b4a49c99e252173f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106986459"
---
# <a name="msiembeddedui-table"></a>MsiEmbeddedUI 資料表

MsiEmbeddedUI 資料表會定義內嵌在 Windows Installer 套件中的使用者介面。

**[Windows Installer 4.0 或更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此資料表。

MsiEmbeddedUI 資料表具有下列資料行。



| Column        | 類型                               | 答案 | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [識別碼](identifier.md)       | Y   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| 屬性    | [整數](integer.md)             | N   | N        |
| MessageFilter | [DoubleInteger](doubleinteger.md) | N   | Y        |
| 資料          | [二進位](binary.md)               | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

資料表的主要索引鍵。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

在資料行中接收二進位資訊之檔案的名稱。 需要包含副檔名的檔案名。 例如，名稱 *embeddedui.dll* 是可接受的，但 *embeddedui* 是無法接受的。 名稱可以當地語系化。 這個欄位可以包含簡短的檔案名或長檔名，但不能同時包含這兩個名稱。 此欄位的格式與 [Filename](filename.md) 資料行資料類型類似，不同之處在于 \| 不提供簡短的檔案名/完整檔案名語法的垂直線 () 分隔符號。 由於某些網頁伺服器可能會區分大小寫，因此檔案名應該完全符合原始程式檔的大小寫，以確保支援網際網路下載。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

資料行中資料的相關資訊。 此欄位中的值可以包含下列一或多個常數。



| 常數                      | 十六進位 | Decimal | 意義                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| None                          | 0x00        | 0       | 檔案不是使用者介面的 DLL 檔案。 它可能是使用者介面所使用的資源檔。                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | 使用者介面的主要 DLL 檔。 資料表中不能有一個以上的資料列以這個屬性標記。 如果有多個資料列是以這個屬性標記，就會發生錯誤，而且無法保證使用的是哪一個 DLL。 |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | 讓安裝程式在基本的 UI 層級安裝期間叫用內嵌 UI。 如果安裝程式未與 **msidbEmbeddedUI** 屬性結合，則會忽略此屬性。                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

指定傳送至使用者介面 DLL 的訊息類型。 此資料行只與具有 **msidbEmbeddedUI** 屬性的資料列有關。 如果資料列參考資源檔，而屬性的值為 null，則此欄位應為 null。 如果資料列參考使用者介面 DLL，則此資料行中的值不應為 null。

此資料行中的值可以是下列值的組合。 安裝程式會忽略任何其他值。



| 常數                           | 十六進位 | Decimal   | Description                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | 提前終止。                                                                                       |
| **INSTALLLOGMODE \_ 錯誤**          | 0x00002     | 2         | 錯誤訊息。                                                                                              |
| **INSTALLLOGMODE \_ 警告**        | 0x00004     | 4         | 警告訊息。                                                                                            |
| **INSTALLLOGMODE \_ 使用者**           | 0x00008     | 8         | 使用者訊息。                                                                                               |
| **INSTALLLOGMODE \_ 資訊**           | 0x00010     | 16        | 未記錄狀態訊息。                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | 目前保留使用中的檔案。                                                                                 |
| **INSTALLLOGMODE \_ RESOLVESOURCE**  | 0x00040     | 64        | 來源解析要求。                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | 磁碟空間訊息。                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | 動作開始訊息。                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | 動作資料訊息。                                                                                        |
| **INSTALLLOGMODE \_ 進度**       | 0x00400     | 1024      | 進度訊息。                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2048      | UI 初始化訊息。                                                                                  |
| **INSTALLLOGMODE \_ INITIALIZE**     | 0x01000     | 4096      | 產品安裝開始時傳送的 UI 啟動訊息。                                            |
| **INSTALLLOGMODE \_ 終止**      | 0x02000     | 8192      | 在產品安裝完成之後傳送的 UI 關機訊息。                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | 顯示 UI 對話方塊之前所傳送的訊息。                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | 目前保留使用中的檔案。                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | 產品的安裝隨即開始。 此訊息包含產品的 ProductName 和 ProductCode。              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | 產品的安裝結束。 此訊息包含產品的 ProductName、ProductCode 和 return 值。 |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

此資料行包含二進位資訊。 如果屬性欄位標示了 **msidbEmbeddedUI** 屬性，則此欄位中的資訊必須是 DLL。 如果屬性欄位不是 **msidbEmbeddedUI** 屬性，此欄位中的資訊可以是任何格式的資源檔。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用內嵌使用者介面，安裝程式開發人員必須將此功能撰寫 Windows Installer 套件中。 MsiEmbeddedUI 資料表會定義內嵌的使用者介面。 內嵌 UI 的 DLL 應該匯出 *InitializeEmbeddedUI*、 *EmbeddedUIHandler* 和 *ShutdownEmbeddedUI* 函數。 不支援內嵌使用者介面的封裝可以使用 Windows Installer 內部使用者介面。

若要在內嵌使用者介面上執行 [適用于 Windows 的調試](https://www.microsoft.com/?ref=go) 程式，請使用 [偵錯工具自訂動作](debugging-custom-actions.md)中所述的技術。 將 MsiBreak 的值設定為 MsiEmbeddedUI。

如需內嵌自訂 UI 的範例，請參閱 [使用內嵌 ui](using-an-embedded-ui.md)。

 

 



