---
description: 定義要在 Microsoft Authenticode 驗證專案資料時使用的資料。
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: 'PST_AUTHENTICODEDATA 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990213"
---
# <a name="pst_authenticodedata-structure"></a>PST \_ AUTHENTICODEDATA 結構

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

定義要在 Microsoft Authenticode 驗證專案資料時使用的資料。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

**dwModifiers**
</dt> <dd>

值，這個值會識別其中一個呼叫端必須驗證的修飾詞。



| 值                                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_AC \_ 單一 \_ 呼叫者**</dt> <dt>0</dt> </dl>           | 只有一個層級會在呼叫鏈中 PStore。 呼叫端會通過驗證檢查。 指定的影像是立即呼叫端，而是應用程式 ( .exe) 。<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_AC \_ 最 \_ 上層 \_ 呼叫者**</dt> <dt>1</dt> </dl> | 最上層呼叫端必須通過檢查，但可能有中繼 Dll。 指定的映射不一定是立即呼叫端，而是應用程式 ( .exe) 。<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_AC \_ 立即 \_ 呼叫者**</dt> <dt>2</dt> </dl>  | 立即呼叫端必須通過檢查，但不需要是最上層的進程。 指定的影像是立即呼叫端，而影像可以是應用程式 ( .exe) 或 DLL。<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

寬字元字串的指標，代表憑證 (CA) 的根憑證授權單位。使用 **Null** 來使用任何可用的 CA。

</dd> <dt>

**szIssuer**
</dt> <dd>

代表發出憑證之 CA 的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。

</dd> <dt>

**szPublisher**
</dt> <dd>

代表軟體發行者的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。

</dd> <dt>

**szProgramName**
</dt> <dd>

代表程式名稱的寬字元字串指標。使用 **Null** 來使用任何可用的 CA。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



 

 
