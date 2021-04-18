---
title: 變更使用者資訊的元素
description: 網路管理功能可提供各種不同的資訊層級，以協助變更使用者資訊。
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966039"
---
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="961ed-103">變更使用者資訊的元素</span><span class="sxs-lookup"><span data-stu-id="961ed-103">Changing Elements of User Information</span></span>

<span data-ttu-id="961ed-104">網路管理功能可提供各種不同的資訊層級，以協助變更使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="961ed-105">某些層級需要系統管理許可權才能順利執行。</span><span class="sxs-lookup"><span data-stu-id="961ed-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="961ed-106">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="961ed-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="961ed-107">本主題中的範例程式碼示範如何藉由呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數來變更使用者資訊的數個元素。</span><span class="sxs-lookup"><span data-stu-id="961ed-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-108">此程式碼會使用各種網路管理資訊結構。</span><span class="sxs-lookup"><span data-stu-id="961ed-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="961ed-109">變更使用者資訊時，最好是使用該資訊的特定層級。</span><span class="sxs-lookup"><span data-stu-id="961ed-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="961ed-110">這可防止在使用較低層級值時意外重設不相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="961ed-111">下列程式碼範例說明如何設定一些較常用的層級：</span><span class="sxs-lookup"><span data-stu-id="961ed-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="961ed-112">設定使用者密碼，層級1003</span><span class="sxs-lookup"><span data-stu-id="961ed-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="961ed-113">設定使用者權限，層級1005</span><span class="sxs-lookup"><span data-stu-id="961ed-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="961ed-114">設定使用者主目錄，層級1006</span><span class="sxs-lookup"><span data-stu-id="961ed-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="961ed-115">設定使用者批註欄位，層級1007</span><span class="sxs-lookup"><span data-stu-id="961ed-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="961ed-116">設定使用者旗標，層級1008</span><span class="sxs-lookup"><span data-stu-id="961ed-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="961ed-117">設定使用者腳本路徑，層級1009</span><span class="sxs-lookup"><span data-stu-id="961ed-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="961ed-118">設定使用者授權單位旗標，層級1010</span><span class="sxs-lookup"><span data-stu-id="961ed-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="961ed-119">設定使用者的完整名稱，層級1011</span><span class="sxs-lookup"><span data-stu-id="961ed-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="961ed-120">所有程式碼片段都假設使用者已定義 UNICODE compile 指示詞，並包含適當的 SDK 標頭檔，如下所示：</span><span class="sxs-lookup"><span data-stu-id="961ed-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="961ed-121">設定使用者密碼，層級1003</span><span class="sxs-lookup"><span data-stu-id="961ed-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="961ed-122">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫，將使用者的密碼設定為已知的值。</span><span class="sxs-lookup"><span data-stu-id="961ed-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-123">[**使用者 \_ 資訊 \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="961ed-124">設定使用者權限，層級1005</span><span class="sxs-lookup"><span data-stu-id="961ed-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="961ed-125">下列程式碼片段說明如何使用對 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫，來指定指派給使用者的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="961ed-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-126">[**使用者 \_ 資訊 \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="961ed-127">如需帳戶許可權的詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges) 和 [授權常數](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="961ed-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="961ed-128">設定使用者主目錄，層級1006</span><span class="sxs-lookup"><span data-stu-id="961ed-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="961ed-129">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫來指定使用者主目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="961ed-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-130">目錄可以是硬式編碼的路徑或有效的 Unicode 路徑。</span><span class="sxs-lookup"><span data-stu-id="961ed-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="961ed-131">[**使用者 \_ 資訊 \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="961ed-132">設定使用者批註欄位，層級1007</span><span class="sxs-lookup"><span data-stu-id="961ed-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="961ed-133">下列程式碼片段說明如何藉由呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式來建立批註與使用者之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="961ed-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-134">[**使用者 \_ 資訊 \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="961ed-135">設定使用者旗標，層級1008</span><span class="sxs-lookup"><span data-stu-id="961ed-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="961ed-136">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定使用者旗標。</span><span class="sxs-lookup"><span data-stu-id="961ed-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-137">「 [**使用者 \_ 資訊 \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) 」主題包含旗標的有效值清單以及每個旗標的描述。</span><span class="sxs-lookup"><span data-stu-id="961ed-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="961ed-138">請注意，您 \_ 必須針對 Windows NT、windows 2000、WINDOWS XP 和 LAN Manager 網路設定 UF 腳本旗標。</span><span class="sxs-lookup"><span data-stu-id="961ed-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="961ed-139">嘗試設定其他旗標而不 \_ 在這些網路上設定 UF 腳本，將會導致 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數失敗。</span><span class="sxs-lookup"><span data-stu-id="961ed-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="961ed-140">設定使用者腳本路徑，層級1009</span><span class="sxs-lookup"><span data-stu-id="961ed-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="961ed-141">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定特定使用者的登入腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="961ed-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-142">腳本檔案可以是。CMD 檔案、。EXE 檔案或。.BAT 檔案。</span><span class="sxs-lookup"><span data-stu-id="961ed-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="961ed-143">字串也可以是 null。</span><span class="sxs-lookup"><span data-stu-id="961ed-143">The string can also be null.</span></span> <span data-ttu-id="961ed-144">[**使用者 \_ 資訊 \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="961ed-145">設定使用者授權單位旗標，層級1010</span><span class="sxs-lookup"><span data-stu-id="961ed-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="961ed-146">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫來設定使用者的操作員許可權旗標。</span><span class="sxs-lookup"><span data-stu-id="961ed-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-147">「 [**使用者 \_ 資訊 \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) 」主題包含旗標的有效值清單以及每個旗標的描述。</span><span class="sxs-lookup"><span data-stu-id="961ed-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="961ed-148">設定使用者的完整名稱，層級1011</span><span class="sxs-lookup"><span data-stu-id="961ed-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="961ed-149">下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定使用者的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="961ed-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="961ed-150">[**使用者 \_ 資訊 \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="961ed-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 