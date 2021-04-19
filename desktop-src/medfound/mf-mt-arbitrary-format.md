---
description: 使用 Advanced Systems 格式之二進位資料流程的其他格式資料 (ASF) 檔。
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: 'MF_MT_ARBITRARY_FORMAT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990309"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>MF \_ MT \_ 任意 \_ 格式屬性

使用 Advanced Systems 格式之二進位資料流程的其他格式資料 (ASF) 檔。

## <a name="data-type"></a>資料類型

**位元組\[\]**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="remarks"></a>備註

應用程式可以使用二進位資料流程來保存自訂資料類型。 ASF 媒體來源會將此屬性的值視為不透明 blob。 [**MT \_ 任意 \_ 標頭**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)結構的 **formattype** 成員定義格式資料的版面配置。

在資料流程類型為 **ASF \_ 二進位 \_ 媒體** 的檔案中，此結構對應于資料流程屬性物件中特定類型資料的格式資料欄位。 如需詳細資訊，請參閱 ASF 規格。

> [!Note]  
> 在 Windows Media 格式 SDK 中，二進位資料流程稱為 *任意資料流程* 或 *任意* 資料流程。

 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[MF \_ MT \_ 任意 \_ 標頭](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




