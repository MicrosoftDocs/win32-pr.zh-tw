---
description: 建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: 'NDdeShareAdd 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0a02381fad8412c7ada0c337c21e633ffa6793887a720ec504f1dfa3d78d9ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602138"
---
# <a name="nddeshareadd-function"></a>NDdeShareAdd 函式

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。

## <a name="syntax"></a>語法


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

要修改其 DSDM 的伺服器名稱。

</dd> <dt>

*nLevel* \[在\]
</dt> <dd>

資訊層級。 此參數必須是2。

</dd> <dt>

*pSD* \[在\]
</dt> <dd>

要與此共用相關聯之 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構的指標，以及將在後續起始至此共用時執行的存取檢查。 這個參數可以是 **Null**，在此情況下，DSDM 會建立預設安全描述項，將「完全控制」授與擁有者，並將「讀取和連結」授與所有人。

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

[**NDDESHAREINFO**](nddeshareinfo-str.md)結構的指標，此結構會定義與所建立之 DDE 共用相關聯的 ApplicationTopic 清單以及其他參數。 此參數不可以是 **Null**。

</dd> <dt>

*cBufSize* \[在\]
</dt> <dd>

*LpBuffer* 結構的大小（以位元組為單位）。 此參數不可以是零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。

## <a name="remarks"></a>備註

在用戶端可以連線到 DDE 共用之前，必須先使用 [**NDdeSetTrustedShare**](nddesettrustedshare.md)來信任它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeShareAddW** (Unicode) 和 **NDdeShareAddA** (ANSI) <br/>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

