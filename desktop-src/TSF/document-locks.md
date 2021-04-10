---
title: 檔鎖定
description: 檔鎖定
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- 文字服務架構 (TSF) 、檔鎖定
- TSF (文字服務架構) ，檔鎖定
- 啟用 TSF 的應用程式，檔鎖定
- 檔鎖定
- '文字服務架構 (TSF) ，應用程式字元位置 (ACP) '
- 'TSF (文字服務架構) ，應用程式字元位置 (ACP) '
- '啟用 TSF 的應用程式，應用程式字元位置 (ACP) '
- '應用程式字元位置 (ACP) '
- 'ACP (應用程式字元位置) '
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183259"
---
# <a name="document-locks"></a>檔鎖定

## <a name="the-document-lock-protocol"></a>檔鎖定通訊協定

若要要求 ACP 型應用程式的檔鎖定，TSF 管理員會呼叫 [ITextStoreACP：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)。 針對以錨點為基礎的應用程式，TSF 管理員會呼叫 [ITextStoreAnchor：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)。 應用程式會藉由呼叫 [ITextStoreACPSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP 型應用程式) 或 [ITextStoreAnchorSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (以錨點為基礎的應用程式) **RequestLock** 內，來授與檔鎖定。 鎖定只有在 **OnLockGranted** 呼叫期間有效。 當 **OnLockGranted** 傳回時，檔會被視為已解除鎖定。

## <a name="types-of-document-locks"></a>檔鎖定的類型

檔鎖定有兩種類型：唯讀和讀取/寫入。 唯讀鎖定可讓管理員讀取文字，但無法修改或插入文字。 讀取/寫入鎖定可讓管理員讀取、修改和插入文字。 藉由 \_ \_ 在 *DWFLAGS* 中指定 TS LF read 來要求唯讀鎖定。 藉由 \_ \_ 在 *DWFLAGS* 中指定 TS LF READWRITE 來要求讀取/寫入鎖定。

## <a name="asynchronous-and-synchronous-requests"></a>非同步和同步要求

鎖定要求可以是同步或非同步。 管理員會使用 \_ \_ *DWFLAGS* 中的 TS LF 同步旗標來要求同步鎖定。 如果不存在此旗標，則要求是非同步。

## <a name="granting-the-lock"></a>授與鎖定

當呼叫 **RequestLock** 時，應用程式必須判斷檔目前是否已鎖定。 如果檔未鎖定，而且沒有其他原因要拒絕鎖定，應用程式應該將 *phrSession* 設定為 \_ [確定]，然後返回 \_ [確定]。

如果檔已鎖定，而且鎖定要求是同步的，應用程式應該將 *phrSession* 設定為 TS \_ E 同步，並傳回「 \_ 確定」 \_ 。 這表示無法授與同步要求。

如果檔已鎖定，而且鎖定要求是非同步，則應用程式應該將要求排入佇列，將 *phrSession* 設定為 TS \_ S \_ ASYNC，並傳回 S \_ OK。 當檔變成可用時，應用程式應該從佇列中移除要求並呼叫 **OnLockGranted**。 此鎖定要求佇列是選擇性的;有一個應用程式必須支援的案例。 如果檔有唯讀鎖定，則新的鎖定要求是讀取/寫入，而且要求是非同步，因此應用程式已呼叫 **OnLockGranted** ，而造成 **RequestLock** 的重新進入呼叫。 應用程式應該將 *phrSession* 設定為 TS \_ S \_ ASYNC，然後返回 S \_ OK。 對 **OnLockGranted** 的呼叫傳回之後，應用程式應該使用 TS LF READWRITE 再次呼叫 **OnLockGranted** 來處理升級 \_ 要求 \_ 。

## <a name="lock-enforcement"></a>鎖定強制

應用程式必須先確認有適當的鎖定類型，才能允許存取檔。 例如，應用程式應該在允許 [ITextStoreACP：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) 或 [ITextStoreAnchor：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) 繼續進行之前，先確認檔至少有唯讀鎖定。 如果沒有適當的鎖定存在，應用程式應該會傳回 TF \_ E \_ NOLOCK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字存放區](text-stores.md)
</dt> <dt>

[ITextStoreACP：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




