---
description: DVDAdm. RestoreScreenSaver 方法會還原系統螢幕保護裝置設定。
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: RestoreScreenSaver 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696968"
---
# <a name="restorescreensaver-method"></a>RestoreScreenSaver 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.RestoreScreenSaver`方法會還原系統螢幕保護裝置設定。

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

一般而言，DVD 應用程式會在啟動時停用系統的螢幕保護裝置，方法是將 [ [**DisableScreenSaver**](disablescreensaver-property.md) ] 屬性設定為 [true]，然後在透過呼叫關閉 DVD 應用程式時重新啟用螢幕保護裝置 `RestoreScreenSaver` 。 如果應用程式未使用系統的螢幕保護裝置設定，則不需要呼叫這個方法或設定 **DisableScreenSaver** 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



