---
description: 成功完成資料傳輸時所發生的事件。
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Wia. OnTransferComplete 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192803"
---
# <a name="wiaontransfercomplete-event"></a>Wia. OnTransferComplete 事件

成功完成資料傳輸時所發生的事件。

## <a name="syntax"></a>語法


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Item* 
</dt> <dd>

已傳送的 [**專案**](-wia-item.md) 物件。

</dd> <dt>

*路徑* 
</dt> <dd>

已傳送影像的路徑和檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當資料傳輸、影像或音效順利完成時，WIA 會通知腳本或應用程式。 執行 **objWia** \_ **OnTransferComplete ()** 副程式，以允許您的腳本或應用程式回應資料傳輸的完成。

例如，您可能想要讓腳本在傳輸之後顯示影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




