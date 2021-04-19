---
title: IPropertyStorage-NTFS 檔案系統執行
description: 當檔案不是複合檔案時，NTFS 5.0 版會針對 NTFS 磁片區上的檔案提供 IPropertyStorage 介面的執行。
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd Stg.、、NTFS 檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966866"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-NTFS 檔案系統執行

當檔案不是複合檔案時，NTFS 5.0 版會針對 NTFS 磁片區上的檔案提供 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面的執行。

**若要取得 IPropertySetStorage NTFS 檔案系統執行的指標**

1.  使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 執行來呼叫 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 。
2.  使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的 NTFS 執行來呼叫 [**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 。

## <a name="when-to-use"></a>使用時機

使用 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 來管理單一屬性集內的屬性。 其方法支援讀取、寫入和刪除屬性，以及可與屬性識別碼相關聯的選擇性字串名稱。 另一個方法可讓您設定與屬性儲存體相關聯的時間，另一個方法則允許指派 CLSID，用來將其他程式碼（例如使用者介面 (UI) 程式碼）與屬性集建立關聯。 呼叫 [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 方法會提供指向 NTFS 實 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的指標，可讓您列舉集合中的屬性。

## <a name="remarks"></a>備註

NTFS 執行基本上提供與複合檔案執行相同的功能。 如需詳細資訊，請參閱 [IPropertyStorage 複合檔案執行](ipropertystorage-compound-file-implementation.md)。

因為 NTFS 是健全的檔案系統，所以 NTFS 屬性集永遠不會處於不正確的狀態。 當 NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的內容排清到基礎 NTFS 檔案時，即使在作業期間發生失敗（例如例外處理常式終止），全部或全部都不會將狀態寫入檔案作為不可部分完成的作業。 若要以複合檔案執行達到類似的行為，必須在交易模式中開啟父 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面。

只有在存取 NTFS 5.0 磁片區上設定的 NTFS 屬性時，才可以使用此等級的穩定性。 您可以在舊版 NTFS 上存取 NTFS 屬性集 (例如，在 Windows NT 或 Windows 2000 上執行的電腦存取 Windows NT 4.0) 上執行的檔案伺服器電腦上的屬性集，但在發生非預期的失敗時，不保證處於正確的狀態。

雖然 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的 ntfs 執行不支援 transactioning，但 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的 ntfs 實作為支援。 也就是說， **STGM \_ 交易** 可以在 *grfMode* 參數中指定給 **IPropertySetStorage** 的 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)和 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法。 如同在複合檔案執行中，交易模式只適用于簡單屬性儲存體 (在 *grfFlags* 參數) 中指定 **PROPSETFLAG \_ 簡單**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-NTFS 檔案系統執行](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 