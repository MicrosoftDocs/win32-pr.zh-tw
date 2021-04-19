---
description: 取得指定之專案的新資料流程。
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback：： GetNextStream 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967144"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>IWiaTransferCallback：： GetNextStream 方法

取得指定之專案的新資料流程。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*bstrItemName* \[在\]
</dt> <dd>

類型： **BSTR**

指定要為其建立資料流程的專案名稱。

</dd> <dt>

*bstrFullItemName* \[在\]
</dt> <dd>

類型： **BSTR**

指定要為其建立資料流程之專案的完整名稱。

</dd> <dt>

*ppDestination* \[擴展\]
</dt> <dd>

類型： **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

接收新 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當此方法是由影像處理篩選器所執行時，Windows 映像取得 (WIA) 2.0 迷你驅動程式會在映射取得期間呼叫它，以從用戶端取得目的地串流。

篩選準則的 **IWiaTransferCallback：： GetNextStream** 必須委派給應用程式的回呼方法。 此篩選器會使用應用程式回呼的 **IWiaTransferCallback：： GetNextStream** 執行所傳回的資料流程，建立它自己的串流，以傳回到 WIA 2.0 服務。 篩選會在篩選的資料流程呼叫 [IStream：： Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) 方法時完成。

篩選的資料流程無法在每次寫入時，對寫入它的位元組數目做出任何假設，因為未篩選的影像資料可能來自 WIA 2.0 Preview 元件，而不是驅動程式。 WIA 2.0 Preview 元件一律會將整個未篩選的影像資料寫入篩選的資料流程中一次，這表示篩選的資料流程有一個寫入其中的來源。 如果驅動程式和預覽元件都寫入篩選器的資料流程，則篩選的資料流程無法假設它將會在第一次呼叫 [IStream：： write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) 時收到完整標頭，不過它的對應驅動程式一律會先在一個寫入中寫入標頭資料。 也不能假設後續的寫入只包含一條掃描行。 因此，篩選資料流程可能必須計算寫入的位元組數目，以判斷影像資料的開始位置。

影像處理篩選器的 **IWiaTransferCallback：： GetNextStream** 實作為其影像處理所需的屬性（從取得影像的專案）。 篩選不會直接從傳遞至 [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)的 *pWiaItem2* 讀取屬性。 相反地，篩選準則必須在此 WIA 2.0 專案上呼叫 [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) ，才能取得實際的 WIA 2.0 專案。 這是因為所取得的映射實際上可能是 *pWiaItem2* 的子專案。 例如，取得資料夾時，篩選器會使用 *pWiaItem2* 取得 **IWiaTransferCallback：： (GetNextStream** 中 *pWiaItem2* 的子專案。取得資料夾時，驅動程式會傳回 *pWiaItem2*) 的子專案所代表的影像。 當 WIA 2.0 Preview 元件呼叫傳遞子 WIA 2.0 專案的影像處理篩選準則時，也是如此。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
