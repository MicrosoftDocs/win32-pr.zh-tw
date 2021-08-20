---
title: IRootStorage-複合檔案執行
description: IRootStorage 的 COM 複合檔案執行，可讓您支援在低記憶體或磁碟空間不足的情況下儲存檔案。 如需此介面行為方式的詳細資訊，請參閱 IRootStorage。
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20128e749443d19c6418703bf64d93eb763ae25103d677719bb4cb4cd21349a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961196"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage-複合檔案執行

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)的 COM 複合檔案執行，可讓您支援在低記憶體或磁碟空間不足的情況下儲存檔案。 如需此介面行為方式的詳細資訊，請參閱 **IRootStorage**。

## <a name="when-to-use"></a>使用時機

僅使用系統提供的 [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) 執行，以支援在低記憶體的情況下儲存檔案。

## <a name="remarks"></a>備註

您可以呼叫 COM 的 [**IRootStorage：： SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) 實作為另一個檔案的一般另存新檔作業。 不過，這樣做的應用程式可能與未來的 COM 儲存體層代不相容。 為了避免這種可能性，執行另存新檔作業的應用程式應該手動建立第二個複合檔案，並叫用 [**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)。 **IRootStorage：： SwitchToFile** 方法只能在緊急 (的低記憶體或磁碟空間) 情況下使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




