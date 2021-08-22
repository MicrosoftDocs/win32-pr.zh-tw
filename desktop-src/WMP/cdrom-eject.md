---
title: Cdrom. 退出方法
description: 退出方法會從磁片磁碟機中取出 CD 或 DVD。 |Cdrom. 退出方法
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- 退出方法 Windows Media Player
- 退出方法 Windows Media Player、Cdrom 類別
- Cdrom 類別 Windows Media Player、退出方法
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bd1c5a7a79c2a9b76b3a7a1997c43713fe0f3c1ae28e635a235feb82d214ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997678"
---
# <a name="cdromeject-method"></a>Cdrom. 退出方法

**退出** 方法會從磁片磁碟機中取出 CD 或 DVD。

## <a name="syntax"></a>語法


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果磁片磁碟機門已開啟，這個方法會關閉門。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列範例會建立使用 *Cdrom* 的 HTML button 專案。**退出** 以開啟磁片磁碟機規範索引為零之磁片磁碟機的門。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 版本<br/>                  | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**PlayState**](player-playstate.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





