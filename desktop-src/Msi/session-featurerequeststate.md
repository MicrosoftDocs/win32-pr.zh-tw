---
description: FeatureRequestState 屬性是會話物件的讀寫屬性。
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: FeatureRequestState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981354"
---
# <a name="sessionfeaturerequeststate-property"></a>FeatureRequestState 屬性

**FeatureRequestState** 屬性是 [**會話**](session-object.md)物件的讀寫屬性。 您可以使用它來取得功能的目前動作狀態，或要求功能及其子功能的動作變更。 功能必須在 [功能](feature-table.md) 表中命名。 如果要求某項功能的動作狀態變更，則變更功能之所有元件的動作狀態也可能會變更。 由多項功能所共用之元件的動作狀態，會根據新的功能動作狀態進行適當的變更 (請參閱備註) 。 **FeatureRequestState** 屬性也可以藉由指定關鍵字 all （而非特定功能名稱）來一次設定所有功能。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>屬性值

必要的字串，指定要設定之功能的名稱。 若要將所有功能設定為所需的要求狀態，請使用保留的不區分大小寫單字：全部。

## <a name="remarks"></a>備註

呼叫 **FeatureRequestState** 之前，必須先呼叫 [**SetInstallLevel**](session-setinstalllevel.md)方法。

如果目前正在要求此功能的狀態， **FeatureRequestState** 屬性會傳回下列其中一個值。



| 選取狀態名稱         | 意義                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown =-1  | 這項功能不會採取任何動作。 這相當於 null。       |
| msiInstallStateAdvertised = 1 | 即將公告功能。                                          |
| msiInstallStateAbsent = 2    | 即將移除功能。                                             |
| msiInstallStateLocal = 3     | 功能會安裝為執行本機。                              |
| msiInstallStateSource = 4    | 功能是以執行來源的形式安裝。                        |
| msiInstallStateDefault = 5   | 功能是以功能目前的動作狀態重新安裝。 |



 

例如，下列程式會從 VBScript 自訂動作取得 "MyFeature" 的目前狀態。


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



如果正在設定功能的狀態， **FeatureRequestState** 屬性應該設定為下列其中一個值。



| 選取狀態名稱          | 意義                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | 公告此功能。                  |
| msiInstallStateAbsent = 2     | 移除功能。                     |
| msiInstallStateLocal = 3      | 將功能安裝為執行本機。       |
| msiInstallStateSource = 4     | 將功能安裝為從原始碼執行。 |



 

例如，下列來自 VBScript 自訂動作的要求，它會將 "MyFeature" 安裝為在電腦本機上執行。


```VB
Session.FeatureRequestState("MyFeature")=3
```



呼叫 **FeatureRequestState** 時，安裝程式會嘗試將系結至指定功能之每個元件的動作狀態，盡可能設定為最理想的狀態。 不過，在一般情況下，要求無法完全遵守。 例如，如果功能系結至兩個元件（元件 A 和元件 B），則透過 [FeatureComponents](featurecomponents-table.md) 資料表和元件 a 具有 **msidbComponentAttributesLocalOnly** 屬性，而元件 b 具有 **msidbComponentAttributesSourceOnly** 屬性。 在此情況下，如果呼叫 **FeatureRequestState** 時所要求的狀態為 MsiInstallStateLocal 或 msiInstallStateSource，則這兩個元件無法接受此要求。 在此情況下，您可以將元件 A 設為 msiInstallStateLocal，並將元件 B 設定為 msiInstallStateSource，來開啟這兩個元件。

如果有一個以上的功能連結至單一元件，則該元件的最終動作狀態會依照下列方式決定：如果至少有一個功能呼叫要在本機安裝元件，則會安裝 msiInstallStateLocal。 如果至少有一個功能呼叫要從來源媒體執行元件，則會安裝 msiInstallStateSource。 如果至少有一個功能呼叫移除元件，則動作狀態為 msiInstallStateAbsent。 如需如何選取功能以進行安裝的詳細資訊，請參閱 [功能](feature-table.md) 表。

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作階段**](session-object.md)
</dt> <dt>

[功能](feature-table.md)
</dt> </dl>

 

 




