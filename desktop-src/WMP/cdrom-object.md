---
title: Cdrom 物件
description: Cdrom 物件提供一種方式來存取磁片磁碟機中的 CD 或 DVD。
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Cdrom 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104311924"
---
# <a name="cdrom-object"></a>Cdrom 物件

**Cdrom** 物件提供一種方式來存取磁片磁碟機中的 CD 或 DVD。

**Cdrom** 物件支援下列屬性。



| 屬性                                   | 描述                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | 抓取 CD 或 DVD 光碟機號。                                                                                                                   |
| [播放清單](cdrom-playlist.md)             | 抓取 [播放清單](playlist-object.md) 物件，此物件代表 cd 上目前位於 cd 光碟機的曲目，或 DVD 的根層級標題專案。 |



 

**Cdrom** 物件支援下列方法。



| 方法                   | 描述                          |
|--------------------------|--------------------------------------|
| [彈出](cdrom-eject.md) | 從磁片磁碟機中取出 CD 或 DVD。 |



 

**Cdrom** 物件是透過下列方法來存取。



| Object                                        | 方法                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

基於說明的目的，cdromCollection 會在參考語法區段中使用) 專案 (*索引* 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




