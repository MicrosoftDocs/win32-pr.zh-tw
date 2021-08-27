---
description: SafeWia 物件是一種 &\# 0034; 可安全的腳本&\# 0034; 所有 Windows 影像取得 (WIA) 腳本功能的進入點。
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: SafeWia 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473844"
---
# <a name="safewia-object"></a>SafeWia 物件

**SafeWia** 物件是所有 Windows 影像取得 (WIA) 腳本功能的「安全的腳本」進入點。 使用 WIA 腳本模型的任何應用程式都必須建立 **SafeWia** 或 [**WIA**](-wia-wia.md) 物件。 您可以使用該物件來列舉和建立裝置，並接收硬體事件的通知。

## <a name="members"></a>成員

**SafeWia** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SafeWia** 物件有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**建立**](-wia-iwia-create.md) | [**Wia**](-wia-wia.md)物件的 [**Create**](-wia-iwia-create.md)方法會連接到指定的 Wia 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。<br/> |



 

### <a name="properties"></a>屬性

**SafeWia** 物件具有這些屬性。




| 屬性 | 存取類型 | Description | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>裝置</strong></a><br /> | 唯讀<br /> | <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a>物件的集合，代表安裝在電腦上的所有裝置。 唯讀。 <br /><blockquote>[!Note]<br />這個集合是以0為基礎。</blockquote><br /> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Wia**](-wia-wia.md)
</dt> </dl>

 

 




