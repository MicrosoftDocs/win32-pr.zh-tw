---
description: BLOB \_ 字元集 \_ 列舉指出目前的會議 BLOB 所使用的字元集。
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: 'BLOB_CHARACTER_SET 列舉 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995776"
---
# <a name="blob_character_set-enumeration"></a>BLOB \_ 字元集 \_ 列舉

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**BLOB \_ 字元集 \_** 列舉指出目前的會議 BLOB 所使用的字元集。

## <a name="syntax"></a>Syntax


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS \_ ASCII**
</dt> <dd>

標準 ASCII 格式。

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS \_ UTF7**
</dt> <dd>

Unicode 的七位轉換格式。 如需此格式的詳細資訊，請進行網際網路搜尋以取得 RFC 1642。

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**
</dt> <dd>

UCS 轉換格式8。 如需此格式的詳細資訊，請使用網際網路搜尋 ISO (國際標準組織) 和 IEC (國際電子電機委員會) 檔 ISO/IEC JTC1/SC2/WG2 N 1036 （日期為1994年8月1日） WG2 專案編輯器。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                               |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**取得 \_ CharacterSet**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Init**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




