---
description: Record 物件的 ReadStream 方法會從包含資料流程資料的記錄欄位讀取指定的位元組數目。
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: ReadStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998841"
---
# <a name="recordreadstream-method"></a>ReadStream 方法

[**Record**](record-object.md)物件的 **ReadStream** 方法會從包含資料流程資料的記錄欄位讀取指定的位元組數目。

## <a name="syntax"></a>語法


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*領域* 
</dt> <dd>

記錄中值的必要欄位編號（以1為基礎）。

</dd> <dt>

*length* (長度) 
</dt> <dd>

從資料流程中讀取所需的位元組數目。

</dd> <dt>

*format* 
</dt> <dd>

需要資料位元組的解讀和傳回。



| 參數名稱                                                                                                                                                                                                                                                                  | 意義                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | 長度必須是1到4的長整數。<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | 以 **BSTR** 表示的資料，每個字元一個位元組。<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | ANSI 位元組已轉譯成 Unicode **BSTR**。<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | 直接傳回為 **BSTR** 的位元組配對。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回字串，其中包含從記錄欄位讀取之要求的位元組數目。

## <a name="remarks"></a>備註

不存在之欄位的傳回值為空白值。 如果資料流程的位元組數少於所要求的數目，則傳回的字串會適當地縮短。

如需這個方法的範例，請參閱 [將 ANSI 檔案複製到資料庫欄位](copy-ansi-file-into-a-database-field.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




