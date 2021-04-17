---
description: 存取儲存在 COM + 目錄中的資料。
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: 'COMAdminCatalog 類別 (ComAdmin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468393"
---
# <a name="comadmincatalog-class"></a>COMAdminCatalog 類別

存取儲存在 COM + 目錄中的資料。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L "COMAdmin. COMAdminCatalog"                                                                                       |
| 介面 | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>使用時機

您可以使用從 **COMAdminCatalog** 類別建立的物件，開始以程式設計方式存取儲存在 com + 目錄中的 com + 設定資料。 這項資訊的基礎是元件服務管理工具的主控台樹中的資料夾和專案。 **COMAdminCatalog** 類別可讓您存取目錄中的集合、安裝 com + 應用程式和元件、啟動和停止服務，以及連接至遠端伺服器並加以管理。

元件服務管理工具中的資料夾對應至目錄中的集合，您可以使用從 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 類別建立的物件來表示。 資料夾中的專案會對應至集合中的專案，您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件來表示。

並非所有透過 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 和 [**COMAdminCatalogObject**](comadmincatalogobject.md) 公開的集合和專案都可在「元件服務」系統管理工具中使用。

如需特定集合及其屬性的相關資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。

如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。

若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 COM + 系統管理員類型程式庫。 您可以使用 "COMAdmin. COMAdminCatalog" 將 COMAdminCatalog 物件宣告為類別名稱。

在以 Windows XP 發行的 COM + 1.5 中， **COMAdminCatalog** 類別會執行 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) 介面。 不過，在以 Windows 2000 發行的 COM + 1.0 中， **COMAdminCatalog** 類別只會執行 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>ComAdmin。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin .Idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

