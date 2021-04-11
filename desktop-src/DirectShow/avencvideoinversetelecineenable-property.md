---
description: 指定編碼器是否執行反向電視電影。
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: 'AVEncVideoInverseTelecineEnable 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109497"
---
# <a name="avencvideoinversetelecineenable-property"></a>AVEncVideoInverseTelecineEnable 屬性

指定編碼器是否執行反向電視電影。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoInverseTelecineEnable**

## <a name="remarks"></a>備註

如果值為 **VARIANT \_ TRUE**，編碼器會執行反向電視電影。 如果不需要反向電視電影，請將此屬性設定為 **VARIANT \_ FALSE**。 若要在編碼器之外執行反向電視，請將此屬性設定為 **VARIANT \_ FALSE** ，並將 [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) 屬性設定為 eAVEncVideoOutputScan \_ SameAsInput。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




