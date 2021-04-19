---
title: WMDMRIGHTS 結構
description: WMDMRIGHTS 結構描述內容使用權利。
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- WMDMRIGHTS 結構 windows Media 裝置管理員
- PWMDMRIGHTS 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992798"
---
# <a name="wmdmrights-structure"></a>WMDMRIGHTS 結構

**WMDMRIGHTS** 結構描述內容使用權利。

## <a name="syntax"></a>語法


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**dwContentType**
</dt> <dd>

包含內容類型的 **DWORD** 。

</dd> <dt>

**fuFlags**
</dt> <dd>

位欄位，指定要用於內容的許可權選項。



| 值                        | 描述                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAYBACKCOUNT  | 檔案可播放的次數。 |
| WMDM \_ RIGHTS \_ EXPIRATIONDATE | 檔案的到期日。                 |
| WMDM \_ RIGHTS \_ FREESERIALIDS  | 檔案的可用串列識別碼。          |
| WMDM \_ 許可權 \_ GROUPID 群組  | 檔案的識別碼。                      |
| WMDM \_ RIGHTS \_ NAMEDSERIALIDS | 檔案的名稱序列識別碼。         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

位欄位，包含內容的許可權位。



| 值                                     | 描述                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ 許可權 \_ \_ 在電腦上播放 \_                | 內容可以在個人電腦上播放。 |
| WMDM \_ RIGHTS \_ COPY \_ 至 \_ 非 \_ SDMI \_ 裝置 | 內容可以複製到非 SDMI 裝置。   |
| WMDM \_ 許可權 \_ 複製 \_ 到 \_ CD                | 內容可以複製到 CD。                |
| WMDM \_ 許可權 \_ 複製 \_ 到 \_ SDMI \_ 裝置      | 內容可以複製到 SDMI 裝置。      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

指定應用程式安全性最小層級的位元組陣列。

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** ，包含內容可轉譯的剩餘時間數。

</dd> <dt>

**ExpirationDate**
</dt> <dd>

[**WMDMDATETIME**](wmdmdatetime.md) 結構，其中包含內容的到期日期和時間。 如果授權沒有到期日， **daylightdate.wyear** 成員會設定為0xffff，而 **WMDMDATETIME** 的所有其他成員則會被忽略。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





