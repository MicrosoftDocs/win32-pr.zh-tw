---
description: Windows 密碼篩選 DLL （Passfilt.dll）會在本機系統帳戶的安全性內容中執行，並協助您篩選網域或本機帳戶密碼。
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: 安裝和註冊密碼篩選 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327163"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>安裝和註冊密碼篩選 DLL

您可以使用 Windows 密碼篩選器來篩選網域或本機帳戶密碼。 若要使用網域帳戶的密碼篩選，請在網域中的每個網域控制站上安裝並註冊 DLL。

請執行下列步驟來安裝您的密碼篩選。 您可以手動執行這些步驟，也可以撰寫安裝程式來執行這些步驟。 您必須是系統管理員或屬於系統管理員群組，才能執行這些步驟。

**安裝和註冊 Windows 密碼篩選 DLL**

1.  將 DLL 複製到網域控制站或本機電腦上的 Windows 安裝目錄。 在標準安裝中，預設資料夾為 \\ Windows \\ System32。 請確定您為32位電腦建立32位密碼篩選 DLL，並為64位電腦建立64位密碼篩選 DLL，然後將它們複製到適當的位置。
2.  若要註冊密碼篩選器，請更新下列系統登錄機碼：

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    如果 *REG_MULTI_SZ* 類型的 **通知封裝** 值存在，請將您的 DLL 名稱新增至現有的值資料。 請勿覆寫現有的值，而且不包含 .dll 副檔名。

    如果 **通知封裝** 值不存在，請加以建立，為它指定 *REG_MULTI_SZ* 類型，然後為值資料指定 DLL 的名稱。 請勿包含 .dll 副檔名。

    **通知封裝** 值可以新增多個套件。

3.  尋找 [密碼複雜性] 設定。

    在主控台中，依序按一下 [ **效能及維護**]、[系統 **管理工具**]、[ **本機安全性原則**]、[ **帳戶原則**]，然後按兩下 [ **密碼原則**]。

4.  若要強制執行預設的 Windows 密碼篩選器和自訂密碼篩選器，請確定已啟用 [ **密碼必須符合複雜性需求** ] 原則設定。 否則，請停用 [ **密碼必須符合複雜性需求** ] 原則設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[密碼篩選程式設計考慮](password-filter-programming-considerations.md)
</dt> <dt>

[強式密碼強制執行和 Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[密碼篩選函數](management-functions.md)
</dt> </dl>

 

 



