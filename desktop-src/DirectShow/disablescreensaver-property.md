---
description: DVDAdm. DisableScreenSaver 屬性會開啟或關閉系統螢幕保護裝置。
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: DisableScreenSaver 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845807"
---
# <a name="disablescreensaver-property"></a>DisableScreenSaver 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 



