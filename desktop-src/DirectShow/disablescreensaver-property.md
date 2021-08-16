---
description: DVDAdm. DisableScreenSaver 屬性會開啟或關閉系統螢幕保護裝置。
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: DisableScreenSaver 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bc714dbbdc3e9b144f2d49cb54871cdf09baad5df39f8e18b962d7fc415d44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821126"
---
# <a name="disablescreensaver-property"></a>DisableScreenSaver 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

屬性會開啟 `DVDAdm.DisableScreenSaver` 或關閉系統螢幕保護裝置。

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>傳回值

傳回布林值，指出是否停用 DVD 播放機應用程式的系統螢幕保護裝置設定;true 表示設定已停用。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，預設值為 true。 在觀看 DVD-Video 光碟時，使用者通常不會在長時間內使用滑鼠或鍵盤。 因此，MSWebDVD ActiveX®控制項依預設會停用系統螢幕保護裝置。 Object

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



