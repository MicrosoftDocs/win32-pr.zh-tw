---
title: READERMODEINFO 結構
description: 包含初始化 DoReaderMode 函數所需的資訊。
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- READERMODEINFO 結構 Windows 控制項
- PREADERMODEINFO 結構指標 Windows 控制項
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 510dc7a763d50b42f06b2510e609e0bc7c3c6f31fa1f4c08393964cef75487fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169118"
---
# <a name="readermodeinfo-structure"></a>READERMODEINFO 結構

\[Windows XP Service Pack 2 (SP2) 可支援 **READERMODEINFO** 。 可能在後續版本中不支援。\]

包含初始化 [**DoReaderMode**](doreadermode.md) 函數所需的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

必要。 結構的大小（以位元組為單位）。 在呼叫 [**DoReaderMode**](doreadermode.md)之前，請將此參數設定為 **sizeof (READERMODE)** 。

</dd> <dt>

**hwnd**
</dt> <dd>

類型： **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

必要。 要用於讀取器模式的視窗控制碼。

</dd> <dt>

**fFlags**
</dt> <dd>

類型： **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

旗標：自訂讀取器強制回應視窗的功能。 此參數可以是 0;否則為下列一或多個值。



| 值                                                                                                                                                                                                                                  | 意義                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | 將游標放在位於 **prc** 指定區域的中央。 如果未指定此旗標，資料指標位置會維持不變。<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_VERTICALONLY**</dt> <dt>0x02</dt> </dl>       | 只允許垂直捲動。<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_HORIZONTALONLY**</dt> <dt>0x04</dt> </dl> | 只允許水準滾動。<br/>                                                                                                     |



 

</dd> <dt>

**中國**
</dt> <dd>

類型： **LPRECT**

</dd> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會指定讀取器強制回應視窗中的捲動區域。 如果這個成員是 **Null**，則會將整個視窗當做捲動區域使用。

</dd> <dt>

**pfnScroll**
</dt> <dd>

類型： **PFNREADERSCROLL**

</dd> <dd>

應用程式定義的 [*ReaderScroll*](readerscroll.md) 回呼函式的指標，用來通知應用程式視窗需要以特定方向進行滾動。

</dd> <dt>

**fFlags**
</dt> <dd>

類型： **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

應用程式定義的 [*TranslateDispatch*](translatedispatch.md) 回呼函式的指標，用來取得傳送至讀取器強制回應視窗之任何訊息的第一個通知。

</dd> <dt>

**lParam**
</dt> <dd>

類型： **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

應用程式所需的其他資訊，由呼叫端在 [*ReaderScroll*](readerscroll.md) 回呼函數中讀取。

</dd> </dl>

## <a name="remarks"></a>備註

未在任何公用標頭中宣告此結構。 若要使用它，您必須在自己的標頭中包含如上所示的宣告。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista，僅 Windows vista \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>          |



 

