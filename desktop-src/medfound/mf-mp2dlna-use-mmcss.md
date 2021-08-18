---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器是否使用多媒體類別排程器服務 (MMCSS) 。
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: 'MF_MP2DLNA_USE_MMCSS 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e824451be89bf4aca485edd2c61ce381f0cf4e0a9d5eefff82bf6c99cef2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104754"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a>MF \_ MP2DLNA \_ 使用 \_ MMCSS 屬性

指定數位客廳網路聯盟 (DLNA) 媒體接收器是否使用多媒體類別排程器服務 (MMCSS) 。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 開始串流之前，請設定屬性。

如果此屬性為 **TRUE**，則 DLNA 媒體接收器會向 MMCSS 註冊其本身。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmp2dlna。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




