---
title: IDirectWriterLock-複合檔案執行
description: IDirectWriterLock 的複合檔案執行提供了一種方法，可讓您以單一寫入器和多個讀取器在直接模式中開啟複合檔案。
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861935a4c373ce03408c0e633e581e56d39623da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671835"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock-複合檔案執行

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)的複合檔案執行提供了一種方法，可讓您以單一寫入器和多個讀取器在直接模式中開啟複合檔案。

您可以使用 STGM direct 旗標，在直接模式中開啟複合檔案 \_ 。 [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)介面會將 STGM \_ READWRITE \| STGM \_ 共用 \_ 拒絕寫入旗標設 \_ 為在直接模式中有效，而不需要快照集複本的額外負荷。

當複合檔案使用 STGM 交易旗標以交易模式開啟時 \_ ，您也可以有多個讀取器和單一寫入器使用 STGM \_ READWRITE \| STGM \_ 共用 \_ 拒絕 \_ 寫入旗標。 不過，在此情況下，會為讀取器建立檔案的快照集複本。 暫存複製通常會產生額外負荷。

## <a name="when-to-use"></a>使用時機

當您在直接模式中開啟儲存體時，請使用系統提供的 [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) 執行 (STGM \_ DIRECT) 與 STGM \_ READWRITE \| STGM \_ 共用 \_ 拒絕 \_ 寫入旗標。

若要取得 [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)的指標，請在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)上呼叫 **QueryInterface** 來取得複合檔案的根儲存物件。

呼叫 [**IDirectWriterLock：： WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) 來取得複合檔案的獨佔寫入權限。 呼叫 [**IDirectWriterLock：： ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) 以釋放獨佔寫入權限。

[**IDirectWriterLock：： HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) 指出檔案目前是否已鎖定。

## <a name="remarks"></a>備註

單一寫入器、多重讀取器功能的複合檔案實作為以範圍鎖定為基礎。 寫入器會取得儲存體的獨佔存取權，以在所有目前的讀取器關閉存放裝置之後寫入。 當寫入器處於作用中狀態時，後續的讀取器無法開啟儲存體。 寫入器會呼叫 [**IDirectWriterLock：： WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) 來取得獨佔寫入存取權。 然後，寫入器必須呼叫 [**IDirectWriterLock：： ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) 來釋放儲存體。

必須先呼叫 [**IDirectWriterLock：： WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) ，才能在這個單一讀取器的多個寫入器模式下撰寫。 嘗試寫入檔案，但不呼叫 **IDirectWriterLock：： WaitForWriteAccess** ，第一個結果是 Stg. \_ E \_ ACCESSDENIED。 即使寫入器一開始開啟檔案，而且沒有讀取器目前開啟檔案，也會傳回此錯誤。

## <a name="marshaling-considerations"></a>封送處理考慮

當複合檔案封送處理至同一部電腦上的另一個進程時，通常會使用自訂封送處理。 封送處理儲存體時，不會考慮存取權限，而且 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 指標會以與原始封送處理常式相同的存取模式和許可權傳遞給新的進程。 如需存取模式的詳細資訊，請參閱 [**STGM 常數**](stgm-constants.md)。 在封送處理期間，不會採取任何鎖定，以確保獨佔寫入存取權。 在此情況下，不會對單一寫入器、多重讀取器模式中開啟的複合檔案強制執行單一寫入器原則。 相反地，強制執行是由複合檔案執行在內部處理。

由於 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 指標會在封送處理期間傳遞至另一個進程，因此兩個進程可能會同時存取相同的複合檔案。 即使呼叫端可能會呼叫 [**IDirectWriterLock：： WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess)取得儲存體的獨佔寫入存取權，但封送處理的版本也可以同時具有存取權。 當單一寫入器存取檔案時，不會強制關閉已封送處理的版本。 在此情況下，複合檔案執行會在內部同步寫入。

如果單一寫入器藉由呼叫來取得獨佔存取權， [**IDirectWriterLock：： WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess)，封送處理的儲存體也有寫入權限，而且不需要呼叫 **IDirectWriterLock：： WaitForWriteAccess**。 這兩個處理常式都有寫入權限，而且同步處理是由內部複合檔案執行所控制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




