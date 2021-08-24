---
description: Windows可攜式裝置支援下列區段資料屬性。
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: '區段屬性屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 21c2386175fe2c3117afd722bd9a6762b605acbc51e299d33934d161974db796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704328"
---
# <a name="section-attribute-properties"></a>區段屬性屬性

Windows可攜式裝置支援下列區段資料屬性。



| 屬性                                             | VarType         | 描述                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 區段 \_ 資料 \_ 長度**                       | **VT \_ UI8**     | 指定所參考物件的長度。                                                                                                                                                                                                                                                                                              |
| **WPD \_ 區段 \_ 資料 \_ 位移**                       | **VT \_ UI8**     | 指定所參考物件之資料的以零為基底的位移。                                                                                                                                                                                                                                                                      |
| **WPD \_ 區段 \_ 資料 \_ 參考的 \_ 物件 \_ 資源** | **VT \_ 不明** | [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) ，其中包含指定指定資源之索引鍵的單一值。此資源是 WPD \_ 區段 \_ 資料 \_ 位移和 WPD \_ 區段 \_ 資料 \_ 長度所參考的物件。<br/> 如果這個屬性不存在， \_ \_ 則會假設為 WPD 資源預設值。<br/> |
| **WPD \_ 區段 \_ 資料 \_ 單位**                        | **VT \_ UI4**     | 指定用於此位移的單位，例如位元組、毫秒等等。這個屬性的可能值定義于 PortableDevice 檔案中的 **WPD \_ 區段 \_ 資料 \_ 單位 \_ 值** 列舉。<br/> 如果未指定任何單位，則會假設為 bytes。<br/>                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




