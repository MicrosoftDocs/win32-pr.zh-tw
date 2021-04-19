---
description: SafeWia 物件是一種 &\# 0034; 可安全的腳本&\# 0034; 所有 Windows 映像取得 (WIA 的進入點) 腳本功能。
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
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970821"
---
# <a name="safewia-object"></a>SafeWia 物件

**SafeWia** 物件是所有 Windows 映像取得 (WIA) 腳本功能的「安全的腳本」進入點。 使用 WIA 腳本模型的任何應用程式都必須建立 **SafeWia** 或 [**WIA**](-wia-wia.md) 物件。 您可以使用該物件來列舉和建立裝置，並接收硬體事件的通知。

## <a name="members"></a>成員

**SafeWia** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SafeWia** 物件有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**創建**](-wia-iwia-create.md) | [**Wia**](-wia-wia.md)物件的 [**Create**](-wia-iwia-create.md)方法會連接到指定的 Wia 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。<br/> |



 

### <a name="properties"></a>屬性

**SafeWia** 物件具有這些屬性。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">屬性</th>
<th style="text-align: left;">存取類型</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>設備</strong></a><br/></td>
<td style="text-align: left;">唯讀<br/></td>
<td style="text-align: left;"><a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a>物件的集合，代表安裝在電腦上的所有裝置。 唯讀。 <br/>
<blockquote>
[!Note]<br />
這個集合是以0為基礎。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Wia**](-wia-wia.md)
</dt> </dl>

 

 




