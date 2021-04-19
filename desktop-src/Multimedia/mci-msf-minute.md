---
title: 'MCI_MSF_MINUTE 宏 (Mciapi) '
description: MCI \_ MSF \_ MINUTE 宏會從包含壓縮分鐘/秒/框架 (MSF) 資訊的參數抓取分鐘元件。
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966542"
---
# <a name="mci_msf_minute-macro"></a>MCI \_ MSF \_ MINUTE 宏

**MCI \_ MSF \_ MINUTE** 宏會從包含壓縮分鐘/秒/框架 (MSF) 資訊的參數抓取分鐘元件。

## <a name="syntax"></a>語法


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwMSF* 
</dt> <dd>

MSF 格式的時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定之 MSF 資訊的分鐘元件。

## <a name="remarks"></a>備註

MSF 格式的時程表示為 **DWORD** 值，具有最小的最小位元組數（包含分鐘）、下一個最不重要的位元組（包含秒），以及下一個包含框架的最小有效位元組。 最重要的位元組未使用。

**MCI \_ MSF \_ MINUTE** 巨集定義如下：


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 宏](mci-macros.md)
</dt> </dl>

 

 





