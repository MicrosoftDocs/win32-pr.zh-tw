---
description: DVDAdm. RestoreScreenSaver 方法會還原系統螢幕保護裝置設定。
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: RestoreScreenSaver 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000039"
---
# <a name="restorescreensaver-method"></a>RestoreScreenSaver 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 



