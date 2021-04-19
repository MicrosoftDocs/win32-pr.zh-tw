---
description: 處理 COM + 管理錯誤
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: 處理 COM + 管理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973392"
---
# <a name="handling-com-administration-errors"></a>處理 COM + 管理錯誤

使用 COMAdmin 物件時所產生的錯誤會以兩種方式報告，如下所示：

-   使用 COMAdmin 程式庫特定的錯誤碼。
-   使用特殊 [**ErrorInfo**](errorinfo.md) 集合中可用的擴充錯誤資訊。

## <a name="error-codes"></a>錯誤碼

您可以處理管理錯誤碼，就像任何 COM 錯誤訊息一樣。 在 Microsoft Visual C++ 中，這些代碼會以 **HRESULT** 值的形式傳回。 在 Microsoft Visual Basic 中，它們會被視為您可以攔截的例外狀況。 針對 c + + 程式設計人員，COM + 系統管理錯誤碼定義于 Winerror.h 中。 針對 Visual Basic 程式設計人員，可以透過 Visual Basic IDE 取得。

## <a name="errorinfo-collection"></a>ErrorInfo 集合

發生錯誤時，會有某種失敗代碼的信號，視錯誤的性質而定，可能會提供更詳細的資訊。 COMAdmin 物件提供延伸的資訊，在不需要詳細的報表（例如，有多個讀取和寫入作業）的情況下，可能會難以判斷失敗的確切原因。

例如，當您在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上使用 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)和 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之類的方法時，您可以針對集合中的每個專案讀取或寫入資料。 可能會發生複雜的錯誤，而且可能很難根據單一數值錯誤碼進行診斷。 因此，COMAdmin 程式庫會透過特殊的集合來提供延伸的錯誤資訊。

當有擴充的錯誤資訊可用時，它會放在與發生錯誤的原創組合相關的 [**ErrorInfo**](errorinfo.md) 集合中。 若要取得錯誤報表，請取得與原創組合相關的 **ErrorInfo** 集合，並檢查它包含的專案。 您可以在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)上使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)來取出 **ErrorInfo** 集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。

當您收到錯誤時，您必須立即取得並填入失敗之集合的 [**ErrorInfo**](errorinfo.md) 集合，而不會對該集合執行任何其他作業。 否則，會重設 **ErrorInfo** 集合，且不會詳細說明該失敗。

[**ErrorInfo**](errorinfo.md)集合中的專案會公開特殊的錯誤報表屬性 MajorRef 和 MinorRef，以詳細說明錯誤的特定原因。 如需詳細資訊，請參閱 **ErrorInfo**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[交易內的 COM + 管理作業](com--administration-operations-within-transactions.md)
</dt> <dt>

[使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



