---
title: IMsRdpDriveCollection 介面
description: 代表磁片磁碟機物件的集合。
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- IMsRdpDriveCollection 介面遠端桌面服務
- IMsRdpDriveCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465988"
---
# <a name="imsrdpdrivecollection-interface"></a>IMsRdpDriveCollection 介面

代表磁片磁碟機物件的集合。

## <a name="members"></a>成員

**IMsRdpDriveCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpDriveCollection** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpDriveCollection** 介面具有這些方法。



| 方法                                                     | 描述                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | 重新整理集合中的物件清單。<br/> |



 

### <a name="properties"></a>屬性

**IMsRdpDriveCollection** 介面具有這些屬性。



| 屬性                                                              | 存取類型          | Description                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | 唯讀<br/> | 抓取位於指定之索引處的磁片磁碟機。<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | 唯讀<br/> | 抓取集合中的物件計數。<br/> |



 

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

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

