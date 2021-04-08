---
title: IMsRdpDeviceV2 DriveLetterBitmap 屬性
description: 包含代表裝置內所含之磁碟機號對應的位位。
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- DriveLetterBitmap 屬性遠端桌面服務
- DriveLetterBitmap 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，DriveLetterBitmap 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685531"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a>IMsRdpDeviceV2：:D riveLetterBitmap 屬性

包含代表裝置內所含之磁碟機號對應的位位。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a>屬性值

包含在裝置內的磁碟機號對應。 值中的每個位都代表一個磁碟機號。 最不重要的位代表磁碟機號 "A"，下一個位代表磁碟機號 "B"，依此類推。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 SP1<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 包含 SP1<br/>                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





