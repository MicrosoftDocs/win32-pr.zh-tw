---
description: SummaryInfo 物件的 Property 屬性會設定或取得摘要資訊資料流程中指定之屬性的值。
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994672"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo 屬性

[**SummaryInfo**](summaryinfo-object.md)物件的 **property** 屬性會設定或取得摘要資訊資料流程中指定之屬性的值。 建立 [**SummaryInfo**](summaryinfo-object.md) 物件時，會讀取屬性，但是在呼叫 [**保存**](summaryinfo-persist.md) 方法之前，都不會寫入屬性。 將屬性設為空白會導致移除;同樣地，要求不存在的屬性會傳回空值。 否則，值可能會以字串、整數或日期 (日期時間) 類型來傳送。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>屬性值

其中一個摘要屬性的必要屬性識別碼。

## <a name="remarks"></a>備註

**標準摘要屬性識別碼**

 (不是列舉) 



| 參數名稱     | 值 | 描述                                       |
|--------------------|-------|---------------------------------------------------|
| PID \_ 字典    | 0     | SummaryInfo 物件不支援的特殊格式 |
| PID \_ 字碼頁      | 1     | VT \_ I2                                            |
| PID \_ 標題         | 2     | VT \_ LPSTR                                         |
| PID \_ 主體       | 3     | VT \_ LPSTR                                         |
| PID \_ 作者        | 4     | VT \_ LPSTR                                         |
| PID \_ 關鍵字      | 5     | VT \_ LPSTR                                         |
| PID \_ 批註      | 6     | VT \_ LPSTR                                         |
| PID \_ 範本      | 7     | VT \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT \_ LPSTR                                         |
| PID \_ EDITTIME      | 10    | VT \_ FILETIME                                      |
| PID \_ LASTPRINTED   | 11    | VT \_ FILETIME                                      |
| PID \_ 建立 \_ DTM   | 12    | VT \_ FILETIME                                      |
| PID \_ LASTSAVE \_ DTM | 13    | VT \_ FILETIME                                      |
| PID \_ PAGECOUNT     | 14    | VT \_ I4                                            |
| PID \_ WORDCOUNT     | 15    | VT \_ I4                                            |
| PID \_ >CHARCOUNT     | 16    | VT \_ I4                                            |
| PID \_ 縮圖     | 17    | \_不支援 VT CF ()                             |
| PID \_ APPNAME       | 18    | VT \_ LPSTR                                         |
| PID \_ 安全性      | 19    | VT \_ I4                                            |



 

**屬性資料類型**

 (不是列舉) 



| 參數名稱 | 值 | 描述                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | 16位整數                                                                           |
| VT \_ I4         | 3     | 32 位元整數                                                                           |
| VT \_ LPSTR      | 30    | String                                                                                   |
| VT \_ FILETIME   | 64    | 日期時間 (FILETIME，轉換成變異時間)                                           |
| VT \_ CF         | 71    | 剪貼簿格式 + 資料，不是由 [**SummaryInfo**](summaryinfo-object.md) 物件處理 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




