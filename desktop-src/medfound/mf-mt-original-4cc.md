---
description: 包含影片資料流程的原始編解碼器 FOURCC。
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: 'MF_MT_ORIGINAL_4CC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944908"
---
# <a name="mf_mt_original_4cc-attribute"></a>MF \_ MT \_ 原始 \_ 4CC 屬性

包含影片資料流程的原始編解碼器 FOURCC。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

根據來源檔案，AVI 媒體來源可能會在其所提供的媒體類型上設定此屬性。

AVI 檔案包含檔案中每個資料流程的資料流程標頭。 AVI 媒體來源會將資料流程標頭轉譯為媒體類型。 針對壓縮的影片串流，資料流程標頭包含可識別影片編解碼器的 FOURCC。 在大多數情況下，AVI 媒體來源會將此 FOURCC 直接轉換成子類型 GUID，如「 [影片子類型 guid](video-subtype-guids.md)」主題所述。 不過，在某些情況下，它會將原始 FOURCC 對應至另一個相等的 FOURCC。 如果是的話，媒體來源會使用 MF \_ MT \_ 原始4CC 屬性，將原始 FOURCC 儲存在媒體類型中 \_ 。

FOURCC 對應會儲存在登錄中的下列機碼底下：

**HKEY \_類別 \_ 根目錄** \\ **MediaFoundation** \\ **MapVideo4cc**

每個專案都是 **DWORD** 值。 專案的名稱是 FOURCC 的十六進位標記法，不含 "0x" 前置詞，且字串中第一個字元的第一個字元會出現。 例如，FOURCC 碼 ' abcd ' 會顯示為 "61626364"。 專案的值是對等的 FOURCC 程式碼。

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
</dt> </dl>

 

 




