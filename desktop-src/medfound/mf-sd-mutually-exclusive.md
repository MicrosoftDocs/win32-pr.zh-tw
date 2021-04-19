---
description: 指定資料流程是否與相同類型的其他資料流程相互排斥。
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: 'MF_SD_MUTUALLY_EXCLUSIVE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984605"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>MF \_ SD \_ 互斥 \_ 屬性

指定資料流程是否與相同類型的其他資料流程相互排斥。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>備註

如果此屬性為 **TRUE** (非零) ，則在相同的呈現中，資料流程與相同類型的其他資料流程（例如音訊或影片）互斥。 例如，如果 AVI 檔案包含多個音訊串流，則會標示為互斥，因為一次只能播放一個音訊串流。

預設值為 **FALSE**。

> [!Note]  
> 這個屬性不會用於 Advanced 系統格式 (ASF) 檔，其具有更精密的方式來表示相互排除準則。 如需詳細資訊，請參閱 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion)。

 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[資料流程描述元屬性](stream-descriptor-attributes.md)
</dt> </dl>

 

 




