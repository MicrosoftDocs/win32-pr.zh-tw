---
description: DLL/COM 重新導向是 Windows XP 上的公司系統管理員所採用的應用程式隔離策略。
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Windows 上的 DLL/COM 重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ce6b55c2a66d298b7b80248613eab7cefe96c25f8f53dd9218966e235ea267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142261"
---
# <a name="dllcom-redirection-on-windows"></a>Windows 上的 DLL/COM 重新導向

DLL/COM 重新導向是 Windows XP 上的公司系統管理員所採用的應用程式隔離策略。

* * Windows server 2008、Windows Vista、Windows Server 2003 和 Windows XP SP2： * * 不建議使用 DLL/COM 重新導向策略，因為使用資訊清單和[並存元件](about-side-by-side-assemblies-.md)的隔離應用程式可能更容易更新及服務。 如果有資訊清單，則會忽略本機檔案的存在。 如果應用程式沒有資訊清單，則使用本機檔案的 DLL/COM 重新導向策略就會運作。

DLL/COM 重新導向會將應用程式系結至元件的本機版本。 本機組件的檔案可以與應用程式私用位置中的系統元件版本分開保存。 系統的元件版本是全域登錄的，且可供任何系結至該元件的任何其他應用程式使用。 元件的本機版本會保留給應用程式的專屬用途。 如有必要，應用程式所使用的元件檔案可以與系統的元件檔同時載入至記憶體。

DLL/COM 重新導向的啟用方式是將特殊檔案連同本機組件檔案的複本安裝到與應用程式可執行檔相同的目錄中。 特殊檔案是以應用程式可執行檔名稱命名並以 local 附加的空白檔案。 例如，若要針對名為 Myapp 的應用程式啟動 DLL/COM 重新導向，必須將本機版本的元件和名為 Myapp.exe 的空檔案複製到包含 Myapp.exe 的資料夾中。 這會將應用程式系結至元件的本機版本，而不是元件的全域共用版本。

當應用程式載入元件檔（例如 DLL 或 .ocx 檔案）時，Windows 首先會在安裝應用程式的. 本機和可執行檔的資料夾中搜尋它。 如果找到，則應用程式會使用該元件檔案，不論應用程式或登錄中定義了任何目錄搜尋路徑。 如果找不到，則會使用定義之搜尋路徑中的元件檔。

安裝公用程式必須執行下列動作，才能使用 DLL/COM 重新導向來安裝應用程式：

-   空白的本機檔案必須複製到與應用程式可執行檔相同的資料夾中。
-   應用程式所使用的所有元件、DLL 和 .ocx 檔案都必須複製到與應用程式可執行檔相同的資料夾中。
-   隔離的 COM 元件必須向 Windows 註冊，如此一來，當元件的不同版本同時載入記憶體時，就不會彼此衝突。 註冊程式會要求，雖然元件的執行可以在版本之間變更，但某些 COM 中繼資料（例如 CLSID、ProgID、類型程式庫和執行緒模型）則不能。
-   如果使用 Windows Installer 安裝應用程式，則可以使用 LockPermissions 資料表來保護應用程式目錄。 一般而言，系統會提供讀取、寫入和執行存取權;所有其他進程僅提供執行和讀取存取權。

 

 



