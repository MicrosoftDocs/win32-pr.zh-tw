---
title: IMsRdpDriveCollection RescanDrives 方法
description: 重新整理集合中的物件清單。 |IMsRdpDriveCollection RescanDrives 方法
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- RescanDrives 方法遠端桌面服務
- RescanDrives 方法遠端桌面服務，IMsRdpDriveCollection 介面
- IMsRdpDriveCollection 介面遠端桌面服務，RescanDrives 方法
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606185"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>IMsRdpDriveCollection：： RescanDrives 方法

重新整理集合中的物件清單。

## <a name="syntax"></a>語法


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vboolDynRedir* \[在\]
</dt> <dd>

預設會套用至任何新探索到的裝置或磁片磁碟機的重新導向狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





