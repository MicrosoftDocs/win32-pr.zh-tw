---
title: IMsRdpDriveV2 DriveLetterIndex 屬性
description: 包含磁片磁碟機的字母索引。
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- DriveLetterIndex 屬性遠端桌面服務
- DriveLetterIndex 屬性遠端桌面服務，IMsRdpDriveV2 介面
- IMsRdpDriveV2 介面遠端桌面服務，DriveLetterIndex 屬性
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935130"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2：:D riveLetterIndex 屬性

包含磁片磁碟機的字母索引。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>屬性值

磁片磁碟機的字母索引。 0 = "A"、1 = "B" 等等。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 SP1<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





