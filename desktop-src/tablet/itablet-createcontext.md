---
description: 建立描述指定之平板電腦裝置的內容物件。
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: ITablet：： CreateCoNtext 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852168"
---
# <a name="itabletcreatecontext-method"></a>ITablet：： CreateCoNtext 方法

建立描述指定之平板電腦裝置的內容物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

Tablet 內容將附加的視窗。

</dd> <dt>

*prcInput* \[在\]
</dt> <dd>

\[在中，唯一\]

筆墨輸入矩形。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

設定 tablet coNtext 選項的旗標。

</dd> <dt>

*pTCS* \[在\]
</dt> <dd>

\[在中，唯一\]

要建立之平板電腦內容的詳細資訊。

</dd> <dt>

*cet* \[在\]
</dt> <dd>

值，這個值會啟用或停用傳送至視窗的內容訊息。

</dd> <dt>

*ppCtx* \[擴展\]
</dt> <dd>

新建立的平板電腦內容指標。

</dd> <dt>

*pTcid* \[in、out\]
</dt> <dd>

可唯一識別平板電腦的值。

</dd> <dt>

*ppPD* \[in、out\]
</dt> <dd>

每個封包中包含哪些資料的相關資訊指標。

</dd> <dt>

*pSink* \[在\]
</dt> <dd>

將傳送通知訊息的 [**ITabletEventSink**](itableteventsink.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

一般而言，應用程式會從 [**ITablet：： GetDefaultCoNtextSettings 方法**](itablet-getdefaultcontextsettings.md)取得預設值、修改值以符合其需求，然後將修改過的設定結構傳遞至 **ITablet：： CreateCoNtext 方法**。

> [!Note]  
> 呼叫 **ITablet：： CreateCoNtext 方法** 時，您必須執行 [**ITabletEventSink 介面**](itableteventsink.md)。

 

*>dwoptions* 參數是一組用來描述內容選項的位旗標。 下表描述這些旗標。



| 旗標名稱                                | 值                                                                                                                                                                                         | 描述                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TCXO \_ 邊界<br/>                  | 0x00000001<br/>                                                                                                                                                                         | 指定平板電腦上的輸入內容將會有邊界。 邊界是指定之輸入區域以外的區域，其中的事件將會對應至輸入區域的邊緣。 這項功能可讓您更輕鬆地在內容邊緣輸入點。<br/> |
| TCXO \_ PREHOOK<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Prehook 會在一般內容和 posthooks 之前取得封包。 他們會依照建立的順序取得封包。<br/>                                                                                                                                                  |
| TCXO 資料 \_ 指標 \_ 狀態<br/>           | 0x00000004<br/>                                                                                                                                                                         | 即使資料指標已啟動，TC 也會傳回封包。 根據預設，在游標關閉時，TC 只會傳回封包。<br/>                                                                                                                                       |
| TCXO \_ 無 \_ 游標 \_ 向下鍵<br/>        | 0x00000008<br/>                                                                                                                                                                         | 當資料指標關閉時，TC 不會傳回封包。<br/>                                                                                                                                                                                                       |
| TCXO \_ 非 \_ 整合式<br/>         | 0x00000010<br/>                                                                                                                                                                         | 內容將不會整合。<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | Posthooks 會在一般的 tablet 內容之後，但在系統內容之前取得封包。 它們會以建立的相反順序取得封包。<br/>                                                                                                                   |
| TCXO \_ 不要 \_ 顯示資料 \_ 指標<br/>      | 0x00000080<br/>                                                                                                                                                                         | TC 不會設定資料指標的位置。<br/>                                                                                                                                                                                                                      |
| TCXO 不會 \_ \_ 驗證 \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | TC 不會針對裝置支援的屬性驗證 tablet 內容設定中傳遞的 GUID。<br/>                                                                                                                                      |
| TCXO \_ 允許 \_ 筆觸<br/>           | 0x00000400<br/>                                                                                                                                                                         | TC 將允許執行筆觸偵測 (預設只允許在系統內容) ，而且用戶端會取得 SE 筆觸 \_ 事件。<br/>                                                                                                               |
| TCXO \_ 允許 \_ 意見反應 \_ 點擊<br/>   | 0x00000800<br/>                                                                                                                                                                         | TC 將允許顯示畫筆意見反應。 根據預設，這只允許在系統內容上使用。<br/>                                                                                                                                                              |
| TCXO \_ 允許 \_ 意見反應 \_ 桶<br/> | 0x00001000<br/>                                                                                                                                                                         | TC 將允許顯示畫筆意見反應。 根據預設，這只允許在系統內容上使用。<br/>                                                                                                                                                              |
| TCXO \_ 全部<br/>                     | TCXO \_ MARGIN \| TCXO \_ PREHOOK \| TCXO 資料 \_ 指標 \_ 狀態 \| TCXO \_ 沒有 \_ 游標 \_ 向下 \| TCXO \_ 非整合式 \_ \| TCXO \_ POSTHOOK TCXO 不顯示資料 \| \_ \_ \_ 指標 TCXO 不 \| \_ \_ 驗證 \_ TCS<br/> | 所有已定義的 tablet coNtext 選項。<br/>                                                                                                                                                                                                                           |
| TCXO \_ 掛勾<br/>                    | TCXO \_ PREHOOK \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | 結合了預先攔截和後置攔截功能。<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet 介面**](itablet.md)
</dt> <dt>

[**內容 \_ 啟用 \_ 類型列舉**](context-enable-type.md)
</dt> <dt>

[**TABLET \_ 內容 \_ 設定結構**](tablet-context-settings.md)
</dt> <dt>

[**封包 \_ 描述結構**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**ITabletCoNtextP 介面**](itabletcontextp.md)
</dt> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 




