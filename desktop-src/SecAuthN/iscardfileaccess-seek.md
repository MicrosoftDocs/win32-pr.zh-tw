---
description: Seek 方法會選取從中進行 (讀取/寫入) 存取的物件。
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: ISCardFileAccess：： Seek 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693228"
---
# <a name="iscardfileaccessseek-method"></a>ISCardFileAccess：： Seek 方法

\[**Seek** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Seek** 方法會選取從中進行 (讀取/寫入) 存取的物件。

## <a name="syntax"></a>語法


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFile* \[在\]
</dt> <dd>

開啟檔案的控制碼。

</dd> <dt>

*搜尋* \[在\]
</dt> <dd>

應開始搜尋的位置。



| 值                                                                                                | 意義                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ SEEK \_ \_ 開頭</dt> </dl> | 開始搜尋。<br/>          |
| <dl> <dt>SC \_ SEEK \_ FROM \_ END </dt> </dl>      | 從結尾開始搜尋。<br/>              |
| <dl> <dt>SC \_ SEEK \_ 相對</dt> </dl>        | 從目前的位置開始搜尋。<br/> |



 

</dd> <dt>

*lOffset* \[在\]
</dt> <dd>

參考物件中的資料物件數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

若要讀取或寫入檔案，請分別呼叫 [**讀取**](iscardfileaccess-read.md) 或 [**寫入**](iscardfileaccess-write.md) 。

如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**讀**](iscardfileaccess-read.md)
</dt> <dt>

[**寫**](iscardfileaccess-write.md)
</dt> </dl>

 

 
