---
title: 相互排除類型
description: 相互排除類型
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows媒體格式 SDK，相互排除
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- 相互排除，類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da546c753696144c68348c61d01473c7d6414290b5971c220ac8c983317b3b15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110268"
---
# <a name="mutual-exclusion-types"></a>相互排除類型

您可以使用相互排除類型來識別設定檔中互斥物件的本質。 相互排除類型可做為 [**IWMMutualExclusion：： GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) 和 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)的參數。

下表列出相互排除類型的識別碼。



| 相互排除類型常數 | GUID                                 |
|--------------------------------|--------------------------------------|
| CLSID \_ WMMUTEX \_ 語言       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ 位元速率        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ 簡報   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ 不明        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**GUID 值**](guid-values.md)
</dt> </dl>

 

 




